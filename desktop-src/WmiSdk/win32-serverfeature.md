---
description: La \_ clase ServerFeature de Win32 representa las características instaladas en un equipo que ejecuta Windows Server.
ms.assetid: fe3bb95c-7f69-47b5-9c3d-771cdc3ed9ca
ms.tgt_platform: multiple
title: Clase Win32_ServerFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ServerFeature
- Win32_ServerFeature.ID
- Win32_ServerFeature.ParentID
- Win32_ServerFeature.Name
api_type:
- DllExport
api_location:
- ServerCompProv.dll
ms.openlocfilehash: 1be8a2ea1d646e9d882febc7c8eba08b69bb69f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707206"
---
# <a name="win32_serverfeature-class"></a>\_Clase Win32 ServerFeature

\[La **clase \_ ServerFeature de Win32** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use las [clases de proveedor de ServerManager deploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]

La **clase \_ ServerFeature de Win32** representa las características instaladas en un equipo que ejecuta Windows Server.

Los desarrolladores y administradores que necesitan automatizar el proceso de determinación de las características instaladas en un conjunto de equipos servidor pueden utilizar esta clase. Las instancias de esta clase no están disponibles en los equipos cliente.

## <a name="syntax"></a>Sintaxis

``` syntax
[Deprecated("No value"), Dynamic, Provider("ServerFeatureProvider"), AMENDMENT]
class Win32_ServerFeature
{
  uint32 ID;
  uint32 ParentID;
  string Name;
};
```

## <a name="members"></a>Miembros

La **clase \_ ServerFeature de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ServerFeature de Win32** tiene estas propiedades.

<dl> <dt>

**Id**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**clave**](key-qualifier.md), [**no \_ null**](optional-qualifiers.md)
</dt> </dl>

IDENTIFICADOR de la característica de servidor. En la lista siguiente se muestran los posibles valores de la propiedad ID:



Value

Nombre

1

[Servidor de aplicaciones](/windows)

2

Servidor web (IIS)

3

[Servicios de multimedia de transmisión por secuencias](/windows)

5

Servidor de fax

6

Servicios de iSCSI y archivo<br/> [cambio de nombre](/windows)<br/>

7

Servicios de impresión y documentos<br/> [cambio de nombre](/windows)<br/>

8

[Servicios de federación de Active Directory (AD FS)](/windows)

9

Active Directory Lightweight Directory Services

10

Active Directory Domain Services

11

[Servicios UDDI](/windows)<br/>

12

[Servidor DHCP](/windows)

13

[Servidor DNS](/windows)

14

Network Policy and Access Services

16

Servicios de certificados de Active Directory

17

Active Directory Rights Management Services

18

[Servicios de Escritorio remoto](/windows)<br/> [cambio de nombre](/windows)<br/>

19

Servicios de implementación de Windows

20

Hyper-V

21

[Windows Server Update Services](/windows)

33

[Clúster de conmutación por error](/windows)

34

[Equilibrio de carga de red](/windows)

36

[Características de .NET Framework 3.5.1](/windows)<br/> [cambio de nombre](/windows)<br/>

37

[Administrador de recursos del sistema de Windows](/windows)

38

Servicio WLAN

39

[Copias de seguridad de Windows Server características](/windows)

40

Servidor WINS

41

Servicio de activación de procesos de Windows

42

[Asistencia remota](/windows)

43

Servicios simples de TCP/IP

44

[Cliente Telnet](/windows)

45

[Servidor Telnet](/windows)

46

[Subsystem for UNIX-Based Applications](/windows)

47

P roxy RPC sobre HTTP

48

Servidor SMTP

49

Message Queue Server

51

[Windows Internal Database](/windows)

52

[Administrador de almacenamiento para redes San](/windows)

53

Monitor de puerto de LPR

55

[Servidor de nombres de almacenamiento de Internet](/windows)

57

[E/s de múltiples rutas](/windows)

58

Cliente TFTP

59

[Servicios SNMP](/windows)

60

[Administrador de almacenamiento extraíble](/windows)

61

Cifrado BitLocker de unidades

62

[Servicios para Network File System](/windows)

63

Cliente de impresión en Internet

64

[Protocolo de resolución de nombres del mismo nivel](/windows)

65

Kit de administración de Connection Manager

66

[Windows PowerShell](/windows)<br/>

67

[Herramientas de administración remota del servidor](/windows)

68

[Experiencia de calidad de audio y vídeo de Windows (qWave)](/windows)

69

[Administración de directivas de grupo](/windows)

71

[Servicio de Index Server](/windows)

72

[Administrador de recursos del servidor de archivos (FSRM)](/windows)

73

Compresión diferencial remota

310

Servicios de Escritura con lápiz y Escritura a mano<br/>

320

[Herramientas de migración de Windows Server](/windows)<br/>

321

[Extensión WinRM de IIS](/windows)<br/>

324

[BranchCache](#branchcache)<br/>

334

[Consola de administración de DirectAccess](/windows)<br/>

335

[Servicio de transferencia inteligente en segundo plano (BITS)](/windows)<br/>

338

[Visor de XPS](/windows)<br/>

339

[Marco biométrico de Windows](/windows)<br/>

340

Compatibilidad con WoW64<br/>

351

[Entorno de scripting integrado (ISE) de Windows PowerShell](/windows)<br/>

352

Windows TIFF IFilter<br/>

404

[Servicios de actualización de Windows Server](/windows)

409

[Servidor de Administración de direcciones IP (IPAM)](/windows)

417

[Windows PowerShell](/windows)

418

[.NET Framework 4.5](/windows)

432

[Servicio de Windows Search](/windows)

438

[Cliente para NFS](/windows)

441

[Desbloqueo de BitLocker en red](/windows)

442

[Extensión IIS Management OData](/windows)

450

[Servicios avanzados de .NET Framework 4.5](/windows)

466

[Características de .NET Framework 4.5](/windows)

468

[Acceso remoto](/windows)<br/>

477

[Infraestructura e interfaces de usuario](/windows)

478

[Infraestructura y herramientas de administración de gráficos](/windows)

481

[Servicios de archivos y almacenamiento](/windows)

485

[Experiencia con Windows Server Essentials](/windows)

488

[DirectPlay](/windows)

Servicios de archivo: servicios de rol (6)

Value

Nombre

100

[Sistema de archivos distribuido](/windows)

101

Espacio de nombres DFS

102

Replicación DFS

103

[Servicio de replicación de archivos](/windows)

104

[Administrador de recursos del servidor de archivos (FSRM)](/windows)

105

[Servicios para Network File System](/windows)

106

[Almacenamiento de instancia única](/windows)

107

[Servicio de Windows Search](/windows)

108

[Servicio de Index Server](/windows)

255

Servidor de archivos

350

BranchCache para archivos de red

431

[Servidor para NFS](/windows)<br/>

434

[Servicio del agente VSS del servidor de archivos](/windows)<br/>

435

[Servidor de destino iSCSI](/windows)<br/>

436

[Desduplicación de datos](/windows)<br/>

437

[Proveedor de almacenamiento del destino iSCSI (proveedores de hardware de VDS y VSS)](/windows)

486

[Carpetas de trabajo](/windows)

AD DS de servicios de rol (10)

Value

Nombre

110

[Controlador de dominio de Active Directory](/windows)

111

[Administración de identidades para UNIX](/windows)

112

[Servidor para servicios de información de red](/windows)

113

[Sincronización de contraseñas](/windows)

294

[Herramientas de administración remota del servidor](/windows)

Streaming de multimedia: servicios de rol (3)

Value

Nombre

120

[Servidor de Windows Media](/windows)

121

[Administración basada en Web](/windows)

122

[Agente de registro](/windows)

ADFS-servicios de rol (8)

Value

Nombre

125

[Servicios de federación de Active Directory (AD FS)](/windows)

126

[Directiva de Servicio de federación](/windows)

127

[Agentes web de AD FS](/windows)

128

[Agente para notificaciones](/windows)

129

[Agente basado en tokens de Windows](/windows)

Servicios de Escritorio remoto de servicios de rol (18)

Value

Nombre

130

Host de sesión de escritorio remoto<br/> [cambio de nombre](/windows)<br/>

131

[Administración de licencias de Escritorio remoto](/windows)<br/> [cambio de nombre](/windows)<br/>

132

Puerta de enlace de escritorio remoto<br/> [cambio de nombre](/windows)<br/>

133

Agente de conexión a Escritorio remoto<br/> [cambio de nombre](/windows)<br/>

134

Acceso web de Escritorio remoto.<br/> [cambio de nombre](/windows)<br/>

322

Host de virtualización de escritorio remoto<br/>

Host de virtualización de Escritorio remoto de los servicios de rol (322)

Value

Nombre

325

[Servicios principales](/windows)<br/>

327

[Escritorio remoto de gráficos virtuales](/windows)<br/>

Servicios de impresión y documentos de servicios de rol (7)

Value

Nombre

135

Servidor de impresión

136

Impresión en Internet

137

Servicio de impresión de LPD

328

[Servidor de digitalización distribuida](/windows)<br/>

Servidor Web (IIS)-servicios de rol (2)

Value

Nombre

140

Servidor Web

141

Características HTTP comunes

142

Contenido estático

143

Documento predeterminado

144

Examinar directorio

145

Errores HTTP

146

Redireccionamiento HTTP

147

Desarrollo de aplicaciones

148

ASP.NET

149

Extensibilidad de .NET

150

ASP

151

CGI

152

Extensiones ISAPI

153

Filtros de ISAPI

154

Inclusión del servidor (SSI)

155

Mantenimiento y diagnóstico

156

Registro HTTP

157

Herramientas de registro

158

Monitor de solicitudes

159

Seguimiento

160

Registro personalizado

161

Registro ODBC

162

Seguridad

163

Autenticación básica

164

Autenticación de Windows

165

Autenticación implícita

166

Autenticación de asignaciones de certificados de clientes

167

Autenticación de asignaciones de certificados de cliente IIS

168

Autorización de URL

169

Filtrado de solicitudes

170

Restricciones de IP y dominio

171

Rendimiento

172

Compresión de contenido estático

173

compresión de contenido dinámico

174

Herramientas de administración

175

Consola de administración de IIS

176

Scripts y herramientas de administración de IIS

177

Servicio de administración

178

Compatibilidad con la administración de IIS 6

179

Compatibilidad con la metabase de IIS 6

180

Compatibilidad con WMI de IIS 6

181

Herramientas de scripting de IIS 6

182

Consola de administración de IIS 6

183

Servicio de publicación FTP<br/>

184

Servidor FTP

185

Consola de administración de FTP<br/>

314

Publicación en WebDAV

316

Servicio FTP<br/>

317

Extensibilidad de FTP<br/>

336

Núcleo de web hospedable de IIS<br/>

413

[ASP.NET 4,5](/windows)

414

[Extensibilidad de .NET 4.5](/windows)

445

[appialization](/windows)

446

[compatibilidad centralizada con los certificados SSL](/windows)

447

[Protocolo WebSocket](/windows)

Message Queue Server: características (49)

Value

Nombre

190

Servicios de Message Queue Server

191

Message Queuing Server

192

Integración del servicio de directorio

193

Desencadenadores de Message Queue Server

194

Compatibilidad con HTTP

195

Servicio de enrutamiento

196

[Compatibilidad con clientes de Windows 2000](/windows)<br/>

197

Proxy DCOM de Message Queue Server

228

Compatibilidad con multidifusión

Servicios de certificados de Active Directory: servicios de rol (16)

Value

Nombre

200

Entidad de certificación

201

Inscripción web de entidad de certificación

202

Servicio de respuesta en línea

204

Servicio de inscripción de dispositivos de red

318

[Servicio web de inscripción de certificados](/windows)<br/>

319

[Servicio web de directivas de inscripción de certificados](/windows)<br/>

Servicios de acceso y directivas de redes: servicios de rol (14)

Value

Nombre

205

[Servidor de directivas de redes](/windows)

206

[VPN](#vpn)

207

[Servicios de acceso remoto](/windows)

208

[Enrutamiento](#routing)

210

[Autoridad de registro de mantenimiento](/windows)

250

[Protocolo de autorización de credenciales de host](/windows)

Servicios UDDI: servicios de rol (11)

Value

Nombre

215

[Aplicación web de Servicios UDDI](/windows)<br/>

216

[Base de datos de Servicios UDDI](/windows)<br/>

Servicio de activación de procesos de Windows: servicios de rol (41)

Value

Nombre

217

API de configuración

218

Entorno .NET

219

Modelo de proceso

.NET Framework 3.5.1-características (36)

Value

Nombre

220

.NET Framework 3.5.1<br/> [cambio de nombre](/windows)<br/>

221

Activación WCF

222

Activación de HTTP

223

Activación no HTTP

227

Visor de XPS<br/>

Servicios SNMP-características (59)

Value

Nombre

224

[Servicio SNMP](/windows)

225

[Proveedor WMI de SNMP](/windows)

Servicios de aplicación de servicios de rol

Value

Nombre

230

[.NET Framework 3.5.1](/windows)<br/> [cambio de nombre](/windows)<br/>

231

[Compatibilidad con servidor web (IIS)](/windows)

232

[Acceso de red COM+](/windows)

233

[Uso compartido de puertos TCP](/windows)

234

[Compatibilidad con el servicio WAS (Windows Process Activation Service)](/windows)

235

[Activación HTTP](/windows)

236

[Activación de Message Queue Server](/windows)

237

[Activación TCP](/windows)

238

[Activación de canalizaciones con nombre](/windows)

239

[Transacciones distribuidas](/windows)

240

[Transacciones remotas entrantes](/windows)

241

[Transacciones remotas salientes](/windows)

242

[Transacciones WS-Automatic](/windows)

353

[Extensiones de servidor de aplicaciones para .NET 4,0](/windows)<br/>

Servicios de implementación de Windows: rol (19)

Value

Nombre

251

Servidor de implementación

252

Servidor de transporte

Active Directory Rights Management Services de servicios de rol (17)

Value

Nombre

253

Servidor de Active Directory Rights Management

254

Compatibilidad con la federación de identidades

Herramientas de administración remota del servidor (67)

Value

Nombre

256

[Herramientas de administración de roles](/windows)

257

[Herramientas de AD DS](/windows)<br/> [cambio de nombre](/windows)<br/>

258

[AD LDS herramientas de Snap-Ins y Command-Line](/windows)<br/> [cambio de nombre](/windows)<br/>

259

Herramientas de servicios de certificados de Active Directory

260

[Network Policy and Access Services](/windows)

261

Herramientas de Servicios de impresión y documentos<br/> [cambio de nombre](/windows)<br/>

262

[Active Directory Rights Management Services](/windows)

263

[Herramientas de Servicios de Escritorio remoto](/windows)<br/> [cambio de nombre](/windows)<br/>

264

Herramientas de Servicios de implementación de Windows

265

[Herramientas de administración de características](/windows)

266

Herramientas de cifrado de unidad BitLocker

267

Herramientas de extensiones de servidor BITS

268

[Herramientas de clústeres de conmutación por error](/windows)

269

Herramientas de equilibrio de carga de red

270

Herramientas del servidor SMTP

273

[Herramientas del servidor DNS](/windows)

277

Herramientas de Servicios de archivo

278

Herramientas de Sistema de archivos distribuido

279

Herramientas del Administrador de recursos del servidor de archivos

280

[Servicios para herramientas del sistema de archivos de red](/windows)

281

Herramientas del servidor Web (IIS)

284

[Herramientas del host de sesión Escritorio remoto](/windows)<br/> [cambio de nombre](/windows)<br/>

285

Herramientas de puerta de enlace de Escritorio remoto<br/> [cambio de nombre](/windows)<br/>

286

Herramientas de licencias de Escritorio remoto<br/> [cambio de nombre](/windows)<br/>

288

Herramientas del servidor de fax

290

Herramientas del servidor WINS

291

[Herramientas de Servicios UDDI](/windows)<br/>

292

Herramientas de entidad de certificación

293

Herramientas de respuesta en línea

297

[Herramientas de Servidor para NIS](/windows)

299

[Complementos y herramientas de línea de comandos de AD DS](/windows)<br/> [cambio de nombre](/windows)<br/>

300

[Centro de administración de Active Directory](/windows)

301

Herramientas de Hyper-V

323

[Visor de contraseñas de recuperación de BitLocker](/windows)<br/>

326

[Utilidades de administración de Cifrado de unidad BitLocker](/windows)<br/>

329

[Herramientas de AD DS y AD LDS](/windows)<br/>

330

Centro de administración de Active Directory<br/>

331

[Módulo de Active Directory para Windows PowerShell](/windows)<br/>

337

[Herramientas de Conexión a Escritorio remoto Broker](/windows)<br/>

410

[Cliente de administración de direcciones IP (IPAM)](/windows)

450

[Módulo de Hyper-V para Windows PowerShell](/windows)

462

[Herramientas de Active Directory Rights Management Services](/windows)

465

[Herramienta de administración de almacenamiento y recursos compartidos](/windows)

471

[Herramientas de administración de acceso remoto](/windows)

472

[Módulo de acceso remoto para Windows PowerShell](/windows)

473

[Herramientas de Command-Line y GUI de acceso remoto](/windows)

474

[Herramientas de Windows Server Update Services](/windows)

476

[Herramientas del diagnóstico de licencias de Escritorio remoto](/windows)

479

[Herramientas de SNMP](/windows)

480

[Herramientas de activación de volumen](/windows)

Copias de seguridad de Windows Server-características (39)

Value

Nombre

296

[Copias de seguridad de Windows Server](/windows)

297

[Herramientas de línea de comandos](/windows)

Servicios de Escritura con lápiz y Escritura a mano-características (310)

Value

Nombre

311

[Compatibilidad con entradas manuscritas](/windows)<br/>

312

[Reconocimiento de escritura a mano](/windows)<br/>

Servicio de transferencia inteligente en segundo plano (BITS)-características (335)

Value

Nombre

54

Extensión de servidor IIS

332

[Servidor compacto](/windows)<br/>

Compatibilidad con WOW64: características (340)

Value

Nombre

341

[WoW64](#wow64)<br/>

342

[WoW64 para .NET Framework 2,0 y Windows PowerShell](/windows)<br/>

343

[WoW64 para .NET Framework 2,0](/windows)<br/>

344

[WoW64 para PowerShell](/windows)<br/>

345

[WoW64 para .NET Framework 3,0 y 3,5](/windows)<br/>

346

[WoW64 para servicios de impresión](/windows)<br/>

347

[WoW64 para clúster de conmutación por error](/windows)<br/>

348

[WoW64 para el editor de métodos de entrada](/windows)<br/>

349

[WoW64 para Subsystem for UNIX-Based Applications](/windows)<br/>

Interfaces de usuario e infraestructura: servicios de rol (447)

Value

Nombre

35

[Experiencia de escritorio](/windows)

99

[Shell gráfico de servidor](/windows)

Windows Server Update Services: características (404)

Value

Nombre

405

[API y cmdlets de PowerShell](/windows)

406

[Conectividad SQL Server](/windows)

407

[Servicios WSUS](/windows)

408

[Consola de administración de la interfaz de usuario](/windows)

449

[Conectividad WID](/windows)

Windows PowerShell-características (417)

Value

Nombre

411

[Motor 2,0 de Windows PowerShell](/windows)

412

[Windows PowerShell 3.0](/windows)

448

[Windows PowerShell Web Access](/windows)

1000

[Servicio de configuración de estado deseado de Windows PowerShell](/windows)

.NET Framework 4,5-características (418)

Value

Nombre

419

[.NET Framework 4,5 extendido](/windows)

420

[Servicios WCF](/windows)

421

[Activación HTTP](/windows)

422

[Activación de Message Queuing (MSMQ)](/windows)

423

[Activación de canalización con nombre](/windows)

424

[Activación TCP](/windows)

425

[Uso compartido de puertos TCP](/windows)

429

[ASP.NET 4,5](/windows)

Acceso remoto: rol (468)

Value

Nombre

469

[DirectAccess y VPN (RAS)](/windows)

470

[Enrutamiento](#routing)

Servicios de archivos y almacenamiento: rol (481)

Value

Nombre

482

[Servicios de almacenamiento](/windows)

484

[Herramientas de administración del clúster de conmutación por error](/windows)



 

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Nombre para mostrar de la característica de servidor, como "servidor de archivos", "servidor de impresión" o "experiencia de escritorio".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Número de ID. de la característica de servidor principal. Esta propiedad es 0 si la característica representada por la instancia actual de la clase no tiene una característica primaria.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Lea la [información técnica de administrador del servidor de Windows Server 2008](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) para obtener información sobre las características de servidor.

Las empresas que no usan software de administración que informa de las características del servidor, como System Center Operations Manager con módulos de administración instalados, pueden obtener esa información consultando la clase **\_ ServerFeature de Win32** .

Puede usar las características de comunicación remota de WMI o WinRM para obtener información de características de servidor de los servidores remotos. Para obtener más información acerca de las conexiones remotas DCOM de WMI, consulte [conectarse a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md). Para más información sobre WinRM, consulte Administración remota de Windows.

Windows Server 2012: **Win32 \_ ServerFeature** está en desuso. Para acceder a la información de características de Windows Server mediante programación, puede usar los [cmdlets de administrador del servidor](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10)).

### <a name="windows-server-2012-r2"></a>Windows Server 2012 R2

<dl> <dt>

<span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Servidor de aplicaciones
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Media Services de streaming
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Servicios de federación de Active Directory (AD FS)
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>Servidor DHCP
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>Servidor DNS
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Servicios de Escritorio remoto
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Clústeres de conmutación por error
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Equilibrio de carga de red
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>Características de .NET Framework 3.5.1
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Administrador de recursos del sistema de Windows
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Copias de seguridad de Windows Server características
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Asistencia remota
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Cliente Telnet
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Servidor Telnet
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Subsystem for UNIX-Based Applications
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Windows Internal Database
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Administrador de almacenamiento para redes San
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>Servidor de nombres de almacenamiento de Internet
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>E/s de múltiples rutas
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>Servicios SNMP
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Servicios para Network File System
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Protocolo de resolución de nombres de mismo nivel
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Herramientas de administración remota del servidor
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>Experiencia de calidad de audio y vídeo de Windows
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Administración de directiva de grupo
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Servicio de Index Server
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>Administrador de recursos de servidor de archivos (FSRM)
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Herramientas de migración de Windows Server
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Consola de administración de DirectAccess
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Servicio de transferencia inteligente en segundo plano (BITS)
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Compatibilidad con WoW64
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Servicios de actualización de Windows Server
</dt> <dd>

Adición

</dd> <dt>

<span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>Servidor de administración de direcciones IP (IPAM)
</dt> <dd>

Adición

</dd> <dt>

<span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell
</dt> <dd>

Adición

</dd> <dt>

<span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4,5
</dt> <dd>

Adición

</dd> <dt>

<span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Search Service de Windows
</dt> <dd>

Adición

</dd> <dt>

<span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Cliente para NFS
</dt> <dd>

Adición

</dd> <dt>

<span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>Desbloqueo de red de BitLocker
</dt> <dd>

Adición

</dd> <dt>

<span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Extensión IIS Management OData
</dt> <dd>

Adición

</dd> <dt>

<span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework 4,5 Advanced Services
</dt> <dd>

Adición

</dd> <dt>

<span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>.NET Framework características 4,5
</dt> <dd>

Adición

</dd> <dt>

<span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Infraestructura e interfaces de usuario
</dt> <dd>

Adición

</dd> <dt>

<span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Infraestructura y herramientas de administración de gráficos
</dt> <dd>

Adición

</dd> <dt>

<span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>Servicios de archivos y almacenamiento
</dt> <dd>

Adición

</dd> <dt>

<span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Experiencia con Windows Server Essentials
</dt> <dd>

Adición

</dd> <dt>

<span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Reproducción directa
</dt> <dd>

Adición

</dd> <dt>

<span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>Sistema de archivos distribuido
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>Administrador de recursos de servidor de archivos
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Servicios para Network File System
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Almacenamiento de instancia única
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Search Service de Windows
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Servicio de Index Server
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>Proveedor de almacenamiento del destino iSCSI (proveedores de hardware de VDS y VSS)
</dt> <dd>

Adición

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Carpetas de trabajo
</dt> <dd>

Adición

</dd> <dt>

<span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Controlador de Dominio de Active Directory
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Administración de identidades para UNIX
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Servidor para servicios de información de red
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Sincronización de contraseñas
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Herramientas de administración
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Servidor de Windows Media
</dt> <dd>

Ya no se admite.

</dd> <dt>

<span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Administración basada en Web
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Agente de registro
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>Servicio de federación
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Directiva de Servicio de federación
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>AD FS agentes Web
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Agente basado en tokens de Windows
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Licencias de Escritorio remoto
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Servidor de directivas de redes
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="VPN"></span><span id="vpn"></span>PRIVADA
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Servicios de acceso remoto
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Automático
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Autoridad de registro de mantenimiento
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Protocolo de autorización de credenciales de host
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Visor de XPS
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>Servicio SNMP
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>Proveedor WMI de SNMP
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Compatibilidad con servidor Web (IIS)
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Acceso de red COM+
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Uso compartido de puertos TCP
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Compatibilidad con el servicio de activación de procesos de Windows
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Activación HTTP
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Activación de Message Queue Server
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Activación de TCP
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Activación de canalizaciones con nombre
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Transacciones distribuidas
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Transacciones remotas entrantes
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Transacciones remotas salientes
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>Transacciones WS-Automatic
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Extensiones de servidor de aplicaciones para .NET 4,0
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Herramientas de administración de roles
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>Herramientas de AD DS
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD LDS herramientas de Snap-Ins y Command-Line
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Servicios de acceso y directivas de redes
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Herramientas de Servicios de Escritorio remoto
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Herramientas de administración de características
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Herramientas de clúster de conmutación por error
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>Herramientas del servidor DNS
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Servicios para herramientas del sistema de archivos de red
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Herramientas del servidor Web (IIS)
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Herramientas de Servidor para NIS
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD DS herramientas de Snap-Ins y Command-Line
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Herramientas de AD DS y AD LDS
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Herramientas de Conexión a Escritorio remoto Broker
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>Cliente de administración de direcciones IP (IPAM)
</dt> <dd>

Adición

</dd> <dt>

<span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Módulo de Hyper-V para Windows PowerShell
</dt> <dd></dd> <dt>

<span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Herramienta de Active Directory Rights Management Services
</dt> <dd>

Adición

</dd> <dt>

<span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Herramienta de administración de almacenamiento y recursos compartidos
</dt> <dd>

Adición

</dd> <dt>

<span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Herramientas de administración de acceso remoto
</dt> <dd>

Adición

</dd> <dt>

<span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Módulo de acceso remoto para Windows PowerShell
</dt> <dd>

Adición

</dd> <dt>

<span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>Herramientas de Command-Line y GUI de acceso remoto
</dt> <dd>

Adición

</dd> <dt>

<span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Herramientas de Windows Server Update Services
</dt> <dd>

Adición

</dd> <dt>

<span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Herramientas del diagnóstico de licencias de Escritorio remoto
</dt> <dd>

Adición

</dd> <dt>

<span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>Herramientas de SNMP
</dt> <dd>

Adición

</dd> <dt>

<span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Herramientas de activación de volumen
</dt> <dd>

Adición

</dd> <dt>

<span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Copias de seguridad de Windows Server
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Herramientas de línea de comandos
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Compatibilidad con entradas manuscritas
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Reconocimiento de escritura a mano
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Servidor compacto
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WoW64 para .NET Framework 2,0 y PowerShell
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 para .NET Framework 2,0
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 para PowerShell
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 para .NET Framework 3,0 y 3,5
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 para servicios de impresión
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 para clúster de conmutación por error
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 para el editor de métodos de entrada
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 para Subsystem for UNIX-Based Applications
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Experiencia de escritorio
</dt> <dd>

Adición

</dd> <dt>

<span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Shell gráfico de servidor
</dt> <dd>

Adición

</dd> <dt>

<span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API y cmdlets de PowerShell
</dt> <dd>

Adición

</dd> <dt>

<span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>Conectividad SQL Server
</dt> <dd>

Adición

</dd> <dt>

<span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>Servicios WSUS
</dt> <dd>

Adición

</dd> <dt>

<span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>Consola de administración de la interfaz de usuario
</dt> <dd>

Adición

</dd> <dt>

<span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>Conectividad WID
</dt> <dd>

Adición

</dd> <dt>

<span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Motor 2,0 de Windows PowerShell
</dt> <dd>

Adición

</dd> <dt>

<span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3,0
</dt> <dd>

Adición

</dd> <dt>

<span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShell Web Access
</dt> <dd>

Adición

</dd> <dt>

<span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Servicio de configuración de estado deseado de Windows PowerShell
</dt> <dd>

Adición

</dd> <dt>

<span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4,5 extendido
</dt> <dd>

Adición

</dd> <dt>

<span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>Servicios WCF
</dt> <dd>

Adición

</dd> <dt>

<span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Activación HTTP
</dt> <dd>

Adición

</dd> <dt>

<span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Activación de Message Queuing (MSMQ)
</dt> <dd></dd> <dt>

<span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Activación de canalización con nombre
</dt> <dd>

Adición

</dd> <dt>

<span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Activación de TCP
</dt> <dd>

Adición

</dd> <dt>

<span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Uso compartido de puertos TCP
</dt> <dd>

Adición

</dd> <dt>

<span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4,5
</dt> <dd>

Adición

</dd> <dt>

<span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>Extensibilidad de .NET 4,5
</dt> <dd>

Adición

</dd> <dt>

<span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess y VPN (RAS)
</dt> <dd>

Adición

</dd> <dt>

<span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Automático
</dt> <dd>

Adición

</dd> <dt>

<span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Servicios de almacenamiento
</dt> <dd>

Adición

</dd> <dt>

<span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Herramientas de administración del clúster de conmutación por error
</dt> <dd>

Adición

</dd> <dt>

<span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Herramientas de Active Directory Rights Management Services
</dt> <dd>

Adición

</dd> <dt>

<span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Inicialización de la aplicación
</dt> <dd>

Adición

</dd> <dt>

<span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Compatibilidad de certificados SSL centralizada
</dt> <dd>

Adición

</dd> <dt>

<span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Agente para notificaciones
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Herramientas del host de sesión Escritorio remoto
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>Protocolo WebSocket
</dt> <dd>

ya no se admite

</dd> <dt>

<span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Acceso de red COM+
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>Cambio de nombre de servicios de iSCSI y archivos
</dt> <dd>

Cambiado a servicios de archivo

</dd> </dl>

### <a name="windows-server-2012"></a>Windows Server 2012

<dl> <dt>

<span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Infraestructura e interfaces de usuario
</dt> <dd>

Adición

</dd> <dt>

<span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Servidor para NFS
</dt> <dd>

Adición

</dd> <dt>

<span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>Servicio del agente VSS del servidor de archivos
</dt> <dd>

Adición

</dd> <dt>

<span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>Servidor de destino iSCSI
</dt> <dd>

Adición

</dd> <dt>

<span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Desduplicación de datos
</dt> <dd>

Adición

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Carpetas de trabajo
</dt> <dd>

Quitado

</dd> <dt>

<span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Servicios principales
</dt> <dd>

Agregado solo para esta versión.

</dd> <dt>

<span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Escritorio remoto de gráficos virtuales
</dt> <dd>

Agregado solo para esta versión

</dd> <dt>

<span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Acceso remoto
</dt> <dd>

Adición

</dd> </dl>

### <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

<dl> <dt>

<span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>Servicios UDDI
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Administrador de recursos del sistema de Windows
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Administrador de almacenamiento extraíble
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Servicios de Escritura con lápiz y Escritura a mano
</dt> <dd>

Adición

</dd> <dt>

<span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>Extensión IIS de WinRM
</dt> <dd>

Adición

</dd> <dt>

<span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Consola de administración de DirectAccess
</dt> <dd>

Adición

</dd> <dt>

<span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Servicio de transferencia inteligente en segundo plano (BITS)
</dt> <dd>

Adición

</dd> <dt>

<span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Visor de XPS
</dt> <dd>

Adición

</dd> <dt>

<span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Plataforma de biometría de Windows
</dt> <dd>

Adición

</dd> <dt>

<span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Compatibilidad con WoW64
</dt> <dd>

Adición

</dd> <dt>

<span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Entorno de scripting integrado (ISE) de Windows PowerShell
</dt> <dd>

Adición

</dd> <dt>

<span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>Servicio de replicación de archivos
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache para archivos de red
</dt> <dd>

Adición

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Carpetas de trabajo
</dt> <dd>

Adición

</dd> <dt>

<span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Servidor de digitalización distribuida
</dt> <dd>

Adición

</dd> <dt>

<span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>Servicio de publicación FTP
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>Consola de administración de FTP
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>Servicio FTP
</dt> <dd>

Adición

</dd> <dt>

<span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>Extensibilidad de FTP
</dt> <dd>

Adición

</dd> <dt>

<span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>Núcleo de web Hospedable de IIS
</dt> <dd></dd> <dt>

<span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Compatibilidad con clientes de Windows 2000
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>Servicio web de inscripción de certificados
</dt> <dd>

Adición

</dd> <dt>

<span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>Servicio web de directiva de inscripción de certificados
</dt> <dd>

Adición

</dd> <dt>

<span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>Aplicación Web de servicios UDDI
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>Base de datos de servicios UDDI
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Extensiones de servidor de aplicaciones para .NET 4,0
</dt> <dd>

Adición

</dd> <dt>

<span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>Herramientas de servicios UDDI
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>Utilidades de administración de Cifrado de unidad BitLocker
</dt> <dd>

Adición

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Herramientas de AD DS y AD LDS
</dt> <dd>

Ya no dispone de soporte técnico

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Herramientas de AD DS y AD LDS
</dt> <dd>

Adición

</dd> <dt>

<span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Centro de administración de Active Directory
</dt> <dd>

Adición

</dd> <dt>

<span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Módulo de Active Directory para Windows PowerShell
</dt> <dd>

Adición

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Herramientas de Conexión a Escritorio remoto Broker
</dt> <dd>

Adición

</dd> <dt>

<span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64
</dt> <dd>

Adición

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WoW64 para .NET Framework 2,0 y Windows PowerShell
</dt> <dd>

Adición

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 para .NET Framework 2,0
</dt> <dd>

Adición

</dd> <dt>

<span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 para PowerShell
</dt> <dd>

Adición

</dd> <dt>

<span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 para .NET Framework 3,0 y 3,5
</dt> <dd>

Adición

</dd> <dt>

<span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 para servicios de impresión
</dt> <dd>

Adición

</dd> <dt>

<span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 para clúster de conmutación por error
</dt> <dd>

Adición

</dd> <dt>

<span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 para el editor de métodos de entrada
</dt> <dd>

Adición

</dd> <dt>

<span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 para Subsystem for UNIX-Based Applications
</dt> <dd>

Adición

</dd> <dt>

<span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>Visor de contraseñas de recuperación de BitLocker
</dt> <dd>

Adición

</dd> <dt>

<span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Cambio de nombre de Servicios de impresión y documentos
</dt> <dd>

Servicios de impresión con nombre para esta versión

</dd> <dt>

<span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Cambio de nombre de Servicios de Escritorio remoto
</dt> <dd>

Terminal Services con nombre en esta versión

</dd> <dt>

<span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>Cambio de nombre de características de .NET Framework 3.5.1
</dt> <dd>

Características con nombre .NET Framework 3,0 en esta versión

</dd> <dt>

<span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Escritorio remoto cambio de nombre de host de sesión
</dt> <dd>

Terminal Server con nombre en esta versión

</dd> <dt>

<span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Escritorio remoto cambio de nombre de licencia
</dt> <dd>

Licencias de TS con nombre en esta versión

</dd> <dt>

<span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Escritorio remoto cambio de nombre de puerta de enlace
</dt> <dd>

Puerta de enlace de TS en esta versión

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Cambio de nombre de agente Conexión a Escritorio remoto
</dt> <dd>

Agente de sesiones de TS con nombre en esta versión

</dd> <dt>

<span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Escritorio remoto cambio de nombre de acceso web
</dt> <dd>

Llamado acceso web de TS en esta versión

</dd> <dt>

<span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>Cambio de nombre de .NET Framework 3.5.1
</dt> <dd>

(220) con el nombre características de net FX 3,0 en esta versión

(230) con el nombre Server Core en esta versión

</dd> <dt>

<span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>Cambio de nombre de herramientas de AD DS
</dt> <dd>

Herramientas de Active Directory Domain Services con nombre en esta versión

</dd> <dt>

<span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>Cambio de nombre de AD LDS Snap-Ins y Command-Line Tools
</dt> <dd>

Herramientas de Active Directory Lightweight Directory Services con nombre en esta versión

</dd> <dt>

<span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Cambio de nombre de herramientas de Servicios de impresión y documentos
</dt> <dd>

Herramientas de servicios de impresión con nombre en esta versión

</dd> <dt>

<span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Cambio de nombre de herramientas de Servicios de Escritorio remoto
</dt> <dd>

Herramientas de Terminal Services con nombre en esta versión

</dd> <dt>

<span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Escritorio remoto cambiar el nombre de las herramientas de host de sesión
</dt> <dd>

Herramientas de Terminal Server con nombre en esta versión

</dd> <dt>

<span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Escritorio remoto cambiar el nombre de las herramientas de puerta de enlace
</dt> <dd>

Herramientas de puerta de enlace de TS en esta versión

</dd> <dt>

<span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Cambio de nombre de herramientas de licencias de Escritorio remoto
</dt> <dd>

Herramientas de licencias de TS con nombre en esta versión

</dd> <dt>

<span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>Cambio de nombre de AD DS Snap-Ins y Command-Line Tools
</dt> <dd>

Herramientas del controlador de dominio de Active Directory

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el siguiente script se muestran los nombres de todas las características de servidor del equipo denominado "FABRIKAM". Tenga en cuenta que el equipo de destino debe ejecutar Windows Server 2008 o un sistema operativo de servidor posterior.


```VB
strComputer = "FABRIKAM"

Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")

Set colFeatureList = objWMIService.ExecQuery("SELECT Name FROM Win32_ServerFeature")

For Each objFeature In colFeatureList
   WScript.Echo objFeature.Name

Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>ServerCompProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>ServerCompProv.dll</dt> </dl> |



 

