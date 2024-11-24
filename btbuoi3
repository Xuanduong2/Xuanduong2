using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Demo3
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void listView1_SelectedIndexChanged(object sender, EventArgs e)
        {

        }

        private void btnAdd_Click(object sender, EventArgs e)
        {
            //Tạo một dòng dữ liệu (ListViewItem)
            ListViewItem lvi = new ListViewItem(txtFirstName.Text);
            //Thêm các cột còn lại
            lvi.SubItems.Add(txtLastName.Text);
            lvi.SubItems.Add(txtPhone.Text);
            //đưa dinfg dữ liệu lên listview
             lvNhanVien.Items.Add(lvi);

    
        }
        

        private void btnSua_Click(object sender, EventArgs e)
        {
            if (lvNhanVien.SelectedItems.Count > 0) 
            {
                ListViewItem selectedItem = lvNhanVien.SelectedItems[0]; 
                                                                         
                selectedItem.Text = txtFirstName.Text; 
                selectedItem.SubItems[1].Text = txtLastName.Text; 
                selectedItem.SubItems[2].Text = txtPhone.Text;
            }
            else
            {
                MessageBox.Show("Vui lòng chọn một dòng để sửa!", "Thông báo", MessageBoxButtons.OK, MessageBoxIcon.Warning);
            }
        }

        private void btnDelete_Click(object sender, EventArgs e)
        {
            if(lvNhanVien.SelectedItems.Count > 0) 
    {
                
                DialogResult result = MessageBox.Show("Bạn có chắc chắn muốn xóa dòng này?", "Xác nhận", MessageBoxButtons.YesNo, MessageBoxIcon.Question);
                if (result == DialogResult.Yes)
                {
                    lvNhanVien.Items.Remove(lvNhanVien.SelectedItems[0]); 
                }
            }
    else
            {
                MessageBox.Show("Vui lòng chọn một dòng để xóa!", "Thông báo", MessageBoxButtons.OK, MessageBoxIcon.Warning);
            }
        }



        //
    }
}
