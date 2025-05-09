<mxfile>
	<diagram name="Red Logica - MI EMPRESA S.A.">
		<mxGraphModel dx="800" dy="600" grid="1" gridSize="10" guides="1" tooltips="1" connect="1" arrows="1" fold="1" page="1" pageScale="1" pageWidth="827" pageHeight="1169">
			<root>
				<mxCell id="0"/>
				<mxCell id="1" parent="0"/>
				<!-- Internet -->
				<object label="Internet" id="internet">
					<mxCell style="ellipse;whiteSpace=wrap;html=1;aspect=fixed;fillColor=#FFD700;" vertex="1" parent="1">
						<mxGeometry x="50" y="100" width="80" height="80" as="geometry"/>
					</mxCell>
				</object>
				<!-- Router -->
				<object label="Router de Frontera" id="router">
					<mxCell style="rectangle;whiteSpace=wrap;html=1;fillColor=#DAA520;" vertex="1" parent="1">
						<mxGeometry x="160" y="100" width="100" height="50" as="geometry"/>
					</mxCell>
				</object>
				<!-- Firewall -->
				<object label="Firewall Next-Gen" id="firewall">
					<mxCell style="rectangle;whiteSpace=wrap;html=1;fillColor=#4682B4;" vertex="1" parent="1">
						<mxGeometry x="290" y="90" width="120" height="70" as="geometry"/>
					</mxCell>
				</object>
				<!-- VLAN Usuarios -->
				<object label="VLAN 10: Usuarios" id="vlan10">
					<mxCell style="rectangle;whiteSpace=wrap;html=1;fillColor=#90EE90;" vertex="1" parent="1">
						<mxGeometry x="100" y="220" width="150" height="80" as="geometry"/>
					</mxCell>
				</object>
				<!-- VLAN Servidores -->
				<object label="VLAN 20: Servidores" id="vlan20">
					<mxCell style="rectangle;whiteSpace=wrap;html=1;fillColor=#87CEEB;" vertex="1" parent="1">
						<mxGeometry x="280" y="220" width="150" height="80" as="geometry"/>
					</mxCell>
				</object>
				<!-- VLAN DMZ -->
				<object label="VLAN 30: DMZ" id="vlan30">
					<mxCell style="rectangle;whiteSpace=wrap;html=1;fillColor=#FFB6C1;" vertex="1" parent="1">
						<mxGeometry x="460" y="220" width="150" height="80" as="geometry"/>
					</mxCell>
				</object>
				<!-- VLAN Backup -->
				<object label="VLAN 40: Backup" id="vlan40">
					<mxCell style="rectangle;whiteSpace=wrap;html=1;fillColor=#DDA0DD;" vertex="1" parent="1">
						<mxGeometry x="100" y="340" width="150" height="60" as="geometry"/>
					</mxCell>
				</object>
				<!-- VLAN Seguridad -->
				<object label="VLAN 50: Seguridad" id="vlan50">
					<mxCell style="rectangle;whiteSpace=wrap;html=1;fillColor=#FFA07A;" vertex="1" parent="1">
						<mxGeometry x="280" y="340" width="150" height="60" as="geometry"/>
					</mxCell>
				</object>
				<!-- Conexión entre Internet y Router -->
				<mxCell id="e1" source="internet" target="router" edge="1">
					<mxGeometry relative="1" as="geometry"/>
				</mxCell>
				<!-- Conexión entre Router y Firewall -->
				<mxCell id="e2" source="router" target="firewall" edge="1">
					<mxGeometry relative="1" as="geometry"/>
				</mxCell>
				<!-- Conexión entre Firewall y VLANs -->
				<mxCell id="e3" source="firewall" target="vlan10" edge="1">
					<mxGeometry relative="1" as="geometry"/>
				</mxCell>
				<mxCell id="e4" source="firewall" target="vlan20" edge="1">
					<mxGeometry relative="1" as="geometry"/>
				</mxCell>
				<mxCell id="e5" source="firewall" target="vlan30" edge="1">
					<mxGeometry relative="1" as="geometry"/>
				</mxCell>
				<!-- Conexión interna VLAN Backup -->
				<mxCell id="e6" source="vlan10" target="vlan40" edge="1">
					<mxGeometry relative="1" as="geometry"/>
				</mxCell>
				<!-- Conexión VLAN Seguridad -->
				<mxCell id="e7" source="vlan20" target="vlan50" edge="1">
					<mxGeometry relative="1" as="geometry"/>
				</mxCell>
			</root>
		</mxGraphModel>
	</diagram>
</mxfile>
