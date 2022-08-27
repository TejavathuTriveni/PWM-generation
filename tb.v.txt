`include "proj.v"
module proj_tb;

reg clk;
reg rst;
wire [7:0] count;

proj dut (clk,rst,count);

initial begin
$dumpfile("proj_tb.vcd");
$dumpvars(0,proj_tb);

clk = 0;
rst = 0;

end

initial begin

forever
#5 clk = ~clk;
end



				//initial begin
				//#104 rst=1'b1;
				//#2 rst=1'b0;
				//end



endmodule