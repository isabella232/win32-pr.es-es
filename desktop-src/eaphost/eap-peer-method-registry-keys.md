---
title: Valores del registro del método EAP peer
description: Obtenga información sobre los valores de registro específicos necesarios para los métodos de EAP del mismo nivel. Vea una lista de valores del registro y vea los recursos adicionales disponibles.
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796260a25f824ffe52ada7cdfadfb7a25f05d491
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359426"
---
# <a name="eap-peer-method-registry-values"></a>Valores del registro del método EAP peer

Se requieren valores de registro específicos para los métodos EAP del mismo nivel.

## <a name="eap-peer-method-dll-paths"></a>Rutas de acceso DLL del método EAP del mismo nivel

La ruta de acceso siguiente especifica la ubicación del registro para los archivos dll normales del método EAP del mismo nivel.

**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ Methods \\ *&lt; AuthorId &gt;* \\ * &lt; EapTypeId&gt;***

Por ejemplo, una ruta de acceso de registro de instalación de método EAP dada una **AuthorId** de "311" (que indica que "Microsoft" es el autor) y un **EapTypeId** de "40", aparece de la manera siguiente.

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ Methods \\ 311 \\ 40**

La ruta de acceso siguiente especifica la ubicación del registro para los archivos DLL del método EAP extendido.

> [!Note]  
> Los archivos dll de método EAP extendido se admiten en Windows Vista con Service Pack 1 (SP1) o posterior.

 

**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ Methods \\ *&lt; AuthorId &gt;* \\ 254 \\ *&lt; VendorId &gt;* \\ * &lt; EapTypeId&gt;***

Por ejemplo, una ruta de acceso de registro de instalación de método EAP dada una **AuthorId** de "311" (que indica que "Microsoft" es el autor), un **VendorId** de "311" y un valor de **EapTypeId** de "40", aparece de la manera siguiente.

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ methods \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Para obtener más información sobre la asignación de tipos de método EAP, consulte la sección 6,2 de [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).

 

## <a name="registry-values"></a>Valores del registro

Se requieren los siguientes valores del registro de método del mismo nivel de EAPHost.

-   [PeerDllPath](#peerdllpath)
-   [PeerFriendlyName](#peerfriendlyname)
-   [PeerInvokePasswordDialog](#peerinvokepassworddialog)
-   [PeerInvokeUsernameDialog](#peerinvokeusernamedialog)

Se recomiendan los siguientes valores del registro del método AP peer.

-   [Propiedades](#properties)

Los siguientes valores del registro del método AP del mismo nivel son opcionales.

-   [PeerConfigUIPath](#peerconfiguipath)
-   [PeerIdentityPath](#peeridentitypath)
-   [PeerInteractiveUIPath](#peerinteractiveuipath)
-   [PeerRequireConfigUI](#peerrequireconfigui)

### <a name="peerconfiguipath"></a>PeerConfigUIPath



| Valor constante | PeerConfigUIPath                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ expandir \_ SZ                                                                                                                                        |
| Descripción    | La ruta de acceso al archivo DLL que contiene la implementación del cuadro de diálogo de configuración de usuario. Por ejemplo,% SystemRoot% \\ system32 \\ &lt; nombre \_ de \_ dll &gt; . dll. |



 

### <a name="peerdllpath"></a>PeerDllPath



| Valor constante | PeerDllPath                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ expandir \_ SZ                                                                                 |
| Descripción    | Ruta de acceso al archivo DLL del método EAP. Por ejemplo,% SystemRoot% \\ system32 \\ &lt; nombre \_ de \_ dll &gt; . dll. |



 

### <a name="peerfriendlyname"></a>PeerFriendlyName



| Valor constante | PeerFriendlyName                                                     |
|----------------|----------------------------------------------------------------------|
| Tipo           | Registro \_ SZ                                                              |
| Descripción    | Cadena que contiene el nombre descriptivo (para mostrar) del método EAP. |



 

### <a name="peeridentitypath"></a>PeerIdentityPath



| Valor constante | PeerIdentityPath                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ expandir \_ SZ                                                                                                                                      |
| Descripción    | La ruta de acceso al archivo DLL que contiene la implementación de las funciones de identidad de usuario. Por ejemplo,% SystemRoot% \\ system32 \\ &lt; nombre \_ de \_ dll &gt; . dll. |



 

### <a name="peerinteractiveuipath"></a>PeerInteractiveUIPath



| Valor constante | PeerInteractiveUIPath                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ expandir \_ SZ                                                                                                                                                                                                            |
| Descripción    | La ruta de acceso al archivo DLL que contiene la implementación de la interfaz de usuario interactiva utilizada para obtener información de usuario durante la ejecución del método EAP. Por ejemplo,% SystemRoot% \\ system32 \\ &lt; nombre \_ de \_ dll &gt; . dll. |



 

### <a name="peerinvokepassworddialog"></a>PeerInvokePasswordDialog



| Valor constante | PeerInvokePasswordDialog                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | \_valor DWORD reg                                                                                                                                                                                                                                       |
| Descripción    | 1: para obtener credenciales mediante el cuadro de diálogo contraseña y dominio de EAPHost genérico. 0: para usar un cuadro de diálogo personalizado. Si se usa el cuadro de diálogo genérico, el método [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) establece las credenciales. |



 

### <a name="peerinvokeusernamedialog"></a>PeerInvokeUsernameDialog



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor constante</th>
<th>PeerInvokeUsernameDialog</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tipo</td>
<td>REG_DWORD</td>
</tr>
<tr class="even">
<td>Descripción</td>
<td><ul>
<li>1: para obtener credenciales mediante el cuadro de diálogo nombre de usuario de EAPHost genérico.</li>
<li>0: para usar un cuadro de diálogo personalizado.</li>
</ul>
Si se usa el cuadro de diálogo genérico, el método [<strong>EapPeerSetCredentials</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeersetcredentials) establece las credenciales.</td>
</tr>
</tbody>
</table>



 

### <a name="peerrequireconfigui"></a>PeerRequireConfigUI



| Valor constante | PeerRequireConfigUI                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| Tipo           | \_valor DWORD reg                                                                                 |
| Descripción    | 0 si se implementa un cuadro de diálogo de interfaz de usuario de configuración para este método; 1 si no lo está. |



 

### <a name="properties"></a>Propiedades



| Valor constante | Propiedades                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | \_valor DWORD reg                                                                                                                                                  |
| Descripción    | Los bits de la DWORD se establecen para indicar la compatibilidad con la propiedad. Para obtener una lista de valores admitidos, consulte [**propiedades del método EAP**](eap-method-properties.md). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Claves del registro del método de autenticación de EAP](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[Configuración del registro para tipos de EAP expandidos](registry-keys-for-eap-methods.md)
</dt> <dt>

[Uso de EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 