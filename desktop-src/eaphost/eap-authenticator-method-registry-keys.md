---
title: Valores del Registro Authenticator eap
description: Obtenga información sobre los valores Authenticator del registro de métodos de EAP. Estos valores específicos del Registro son necesarios para los métodos autenticadores eap.
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a710ca6f09914c8d111c42a8323a9c39c51f898
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168454"
---
# <a name="eap-authenticator-method-registry-values"></a>Valores del Registro Authenticator eap

Se requieren valores específicos del Registro para los métodos de autenticación EAP.

## <a name="eap-authenticator-method-dll-paths"></a>Rutas de acceso Authenticator DLL del método EAP

La ruta de acceso siguiente especifica la ubicación del Registro para los archivos DLL normales del método autenticador EAP.

**Métodos eaphost de HKLM \\ System \\ CCS \\ Services \\ \\ \\ *&lt; AuthorId &gt;* \\ * &lt; EapTypeId&gt;***

Por ejemplo, una ruta de acceso de registro de instalación del método autenticador EAP dado un **AuthorId** de "311" (que indica que "Microsoft" es el autor) y un **EapTypeId** de "40", aparece como se indica a continuación.

**HkLM \\ System \\ CCS Services \\ \\ Eaphost Methods \\ \\ 311 \\ 40**

La ruta de acceso siguiente especifica la ubicación del Registro para los archivos DLL extendidos del método autenticador EAP.

**Métodos eaphost de HKLM \\ System \\ CCS \\ Services \\ \\ \\ *&lt; AuthorId &gt;* \\ 254 \\ *&lt; &gt; VendorId* \\ * &lt; VendorType&gt;***

Por ejemplo, una ruta de acceso de registro de instalación del método autenticador EAP dado un **AuthorId** de "311" (que indica que "Microsoft" es el autor), un **VendorId** de "311" y **un EapTypeId** de "40", aparece como se indica a continuación.

**HkLM \\ System \\ CCS Services \\ \\ Eaphost Methods \\ \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Para obtener más información sobre la asignación de tipos de método EAP, vea la sección 6.2 de [RFC 3748.](https://go.microsoft.com/fwlink/p/?linkid=84016)

 

## <a name="registry-values"></a>Valores del Registro

Se requieren los siguientes valores del Registro del método autenticador.

-   [AuthenticatorDllPath](#authenticatordllpath)
-   [AuthenticatorFriendlyName](#authenticatorfriendlyname)

Además de los valores anteriores del Registro, se recomienda el siguiente valor del Registro del método autenticador.

-   [Propiedades](#properties)

Los valores restantes del Registro del método autenticador son opcionales.

-   [ConfigCLSID](#configclsid)
-   [StandaloneSupported](#standalonesupported)

## <a name="authenticatordllpath"></a>AuthenticatorDllPath



| Valor constante | AuthenticatorDllPath                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ EXPAND \_ SZ                                                                                               |
| Descripción    | Ruta de acceso al archivo DLL del método autenticador EAP. Por ejemplo, %SystemRoot% \\ system32 \\ &lt; nombre del archivo \_ DLL \_ &gt;.dll. |



 

## <a name="authenticatorfriendlyname"></a>AuthenticatorFriendlyName



| Valor constante | AuthenticatorFriendlyName                                                          |
|----------------|------------------------------------------------------------------------------------|
| Tipo           | REG \_ SZ                                                                            |
| Descripción    | Cadena que contiene el nombre descriptivo (para mostrar) del método autenticador EAP. |



 

## <a name="configclsid"></a>ConfigCLSID



| Valor constante | ConfigCLSID                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ SZ                                                                                                                               |
| Descripción    | Cadena que contiene el GUID de la clase de configuración para este método autenticador, con el formato {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} |



 

## <a name="properties"></a>Propiedades



| Valor constante | Propiedades                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                                                                                  |
| Descripción    | Los bits de DWORD se establecen para indicar la compatibilidad con la propiedad . Para obtener una lista de los valores admitidos, vea [**Propiedades del método EAP**](eap-method-properties.md). |



 

## <a name="standalonesupported"></a>StandaloneSupported



| Valor constante | StandaloneSupported                                             |
|----------------|-----------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                      |
| Descripción    | 0 si se trata de un método autenticador independiente; 1 si no es así. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Claves del Registro del método del mismo nivel eap](eap-peer-method-registry-keys.md)
</dt> <dt>

[Configuración del Registro para tipos de EAP expandido](registry-keys-for-eap-methods.md)
</dt> <dt>

[Uso de EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




