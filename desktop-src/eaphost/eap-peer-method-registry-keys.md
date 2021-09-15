---
title: Valores del Registro del método del mismo nivel de EAP
description: Obtenga información sobre los valores específicos del Registro necesarios para los métodos del mismo nivel de EAP. Consulte una lista de valores del Registro y vea los recursos disponibles adicionales.
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee42360689a74b3cd11628e6114e80532000b95f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359001"
---
# <a name="eap-peer-method-registry-values"></a>Valores del Registro del método del mismo nivel de EAP

Se requieren valores específicos del Registro para los métodos del mismo nivel de EAP.

## <a name="eap-peer-method-dll-paths"></a>Rutas de acceso DLL del método del mismo nivel de EAP

La ruta de acceso siguiente especifica la ubicación del Registro para los archivos DLL normales del método del mismo nivel de EAP.

**Métodos eaphost de \\ HKLM System \\ CCS \\ Services \\ \\ \\ *&lt; AuthorId &gt;* \\ * &lt; EapTypeId&gt;***

Por ejemplo, una ruta de acceso de registro de instalación del método EAP dada un **AuthorId** de "311" (que indica que "Microsoft" es el autor) y un **EapTypeId** de "40", aparece como sigue.

**HkLM \\ System \\ CCS Services \\ \\ Eaphost Methods \\ \\ 311 \\ 40**

La ruta de acceso siguiente especifica la ubicación del Registro para los archivos DLL extendidos del método EAP.

> [!Note]  
> Los archivos DLL extendidos del método EAP se admiten Windows Vista con Service Pack 1 (SP1) o posterior.

 

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ Methods \\ *&lt; AuthorId &gt;* \\ 254 \\ *&lt; VendorId &gt;* \\ * &lt; EapTypeId&gt;***

Por ejemplo, una ruta de acceso de registro de instalación del método EAP dada un **AuthorId** de "311" (que indica que "Microsoft" es el autor), un **VendorId** de "311" y **un EapTypeId** de "40", aparece como sigue.

**HkLM \\ System \\ CCS Services \\ \\ Eaphost Methods \\ \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Para obtener más información sobre la asignación de tipos de método EAP, vea la sección 6.2 de [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).

 

## <a name="registry-values"></a>Valores del Registro

Se requieren los siguientes valores del Registro del método del mismo nivel EAPHost.

-   [PeerDllPath](#peerdllpath)
-   [PeerFriendlyName](#peerfriendlyname)
-   [PeerInvokePasswordDialog](#peerinvokepassworddialog)
-   [PeerInvokeUsernameDialog](#peerinvokeusernamedialog)

Se recomiendan los siguientes valores del Registro del método del mismo nivel de AP.

-   [Propiedades](#properties)

Los siguientes valores del Registro del método del mismo nivel de AP son opcionales.

-   [PeerConfigUIPath](#peerconfiguipath)
-   [PeerIdentityPath](#peeridentitypath)
-   [PeerInteractiveUIPath](#peerinteractiveuipath)
-   [PeerRequireConfigUI](#peerrequireconfigui)

### <a name="peerconfiguipath"></a>PeerConfigUIPath



| Valor constante | PeerConfigUIPath                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ EXPAND \_ SZ                                                                                                                                        |
| Descripción    | Ruta de acceso al archivo DLL que contiene la implementación del cuadro de diálogo de configuración de usuario. Por ejemplo, %SystemRoot% \\ system32 \\ &lt; nombre del archivo \_ DLL \_ &gt;.dll. |



 

### <a name="peerdllpath"></a>PeerDllPath



| Valor constante | PeerDllPath                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ EXPAND \_ SZ                                                                                 |
| Descripción    | Ruta de acceso al archivo DLL del método EAP. Por ejemplo, %SystemRoot% \\ system32 \\ &lt; nombre del archivo \_ DLL \_ &gt;.dll. |



 

### <a name="peerfriendlyname"></a>PeerFriendlyName



| Valor constante | PeerFriendlyName                                                     |
|----------------|----------------------------------------------------------------------|
| Tipo           | REG \_ SZ                                                              |
| Descripción    | Cadena que contiene el nombre descriptivo (para mostrar) del método EAP. |



 

### <a name="peeridentitypath"></a>PeerIdentityPath



| Valor constante | PeerIdentityPath                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ EXPAND \_ SZ                                                                                                                                      |
| Descripción    | Ruta de acceso al archivo DLL que contiene la implementación de las funciones de identidad de usuario. Por ejemplo, %SystemRoot% \\ system32 \\ &lt; nombre del archivo \_ DLL \_ &gt;.dll. |



 

### <a name="peerinteractiveuipath"></a>PeerInteractiveUIPath



| Valor constante | PeerInteractiveUIPath                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ EXPAND \_ SZ                                                                                                                                                                                                            |
| Descripción    | Ruta de acceso al archivo DLL que contiene la implementación de la interfaz de usuario interactiva que se usa para obtener información de usuario durante la ejecución del método EAP. Por ejemplo, %SystemRoot% \\ system32 \\ &lt; nombre del archivo \_ DLL \_ &gt;.dll. |



 

### <a name="peerinvokepassworddialog"></a>PeerInvokePasswordDialog



| Valor constante | PeerInvokePasswordDialog                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                                                                                                                                                                       |
| Descripción    | 1- para obtener las credenciales mediante el cuadro de diálogo genérico contraseña y dominio de EAPHost. 0 : para usar un cuadro de diálogo personalizado. Si se usa el cuadro de diálogo genérico, el [**método EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) establece las credenciales. |



 

### <a name="peerinvokeusernamedialog"></a>PeerInvokeUsernameDialog




| Valor constante | PeerInvokeUsernameDialog | 
|----------------|--------------------------|
| Tipo | REG_DWORD | 
| Descripción | <ul><li>1 - para obtener las credenciales mediante el cuadro de diálogo de nombre de usuario genérico EAPHost.</li><li>0- para usar un cuadro de diálogo personalizado.</li></ul>Si se usa el cuadro de diálogo genérico, el [<strong>método EapPeerSetCredentials</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) establece las credenciales. | 




 

### <a name="peerrequireconfigui"></a>PeerRequireConfigUI



| Valor constante | PeerRequireConfigUI                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                 |
| Descripción    | 0 si se implementa un cuadro de diálogo de interfaz de usuario de configuración para este método; 1 si no es así. |



 

### <a name="properties"></a>Propiedades



| Valor constante | Propiedades                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                                                                                  |
| Descripción    | Los bits de DWORD se establecen para indicar la compatibilidad con la propiedad . Para obtener una lista de los valores admitidos, vea [**Propiedades del método EAP**](eap-method-properties.md). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Claves del Registro Authenticator eap](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[Configuración del Registro para tipos de EAP expandido](registry-keys-for-eap-methods.md)
</dt> <dt>

[Uso de EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 
