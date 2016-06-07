# METODO-DE-MONTECARLO1
function[y]=plomo(n,iprt)
	m=0;
	for i=1:n;
		x=1;
		for j=1:7;
			teta=rand;
			x =x + cos(pi*teta);
			if x <=0
				break
			elseif x >=5 
				m=m+1;
				break 
			end
		end
		if mod (i,iprt)==0
			y=m/n;
		end
	end
	
end
