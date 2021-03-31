---
title: Valores del registro del método de autenticación de EAP
description: Obtenga información sobre los valores del registro del método de autenticación de EAP. Estos valores de registro específicos son necesarios para los métodos de autenticación de EAP.
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a710ca6f09914c8d111c42a8323a9c39c51f898
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995641"
---
# <a name="eap-authenticator-method-registry-values"></a>Valores del registro del método de autenticación de EAP

Los métodos de autenticación de EAP requieren valores de registro específicos.

## <a name="eap-authenticator-method-dll-paths"></a>Rutas de acceso DLL del método de autenticador EAP

La ruta de acceso siguiente especifica la ubicación del registro para los archivos dll normales del método de autenticación de EAP.

**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ Methods \\ *&lt; AuthorId &gt;* \\ * &lt; EapTypeId&gt;***

Por ejemplo, una ruta de acceso de registro de instalación del método de autenticación de EAP dada una **AuthorId** de "311" (que indica que "Microsoft" es el autor) y un **EapTypeId** de "40", aparece de la manera siguiente.

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ Methods \\ 311 \\ 40**

La ruta de acceso siguiente especifica la ubicación del registro para los archivos DLL del método de autenticador EAP extendido.

**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ Methods \\ *&lt; AuthorId &gt;* \\ 254 \\ *&lt; VendorId &gt;* \\ * &lt; VendorType&gt;***

Por ejemplo, una ruta de acceso de registro de instalación del método de autenticador de EAP dado un valor de **AuthorId** de "311" (que indica que "Microsoft" es el autor), un **VendorId** de "311" y un valor de **EapTypeId** de "40", aparece de la manera siguiente.

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ methods \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Para obtener más información sobre la asignación de tipos de método EAP, consulte la sección 6,2 de [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).

 

## <a name="registry-values"></a>Valores del registro

Se requieren los siguientes valores del registro del método de autenticación.

-   [AuthenticatorDllPath](#authenticatordllpath)
-   [AuthenticatorFriendlyName](#authenticatorfriendlyname)

Además de los valores del registro anteriores, se recomienda el siguiente valor del registro del método de autenticación.

-   [Propiedades](#properties)

Los valores restantes del registro del método de autenticación son opcionales.

-   [ConfigCLSID](#configclsid)
-   [StandaloneSupported](#standalonesupported)

## <a name="authenticatordllpath"></a>AuthenticatorDllPath



| Valor constante | AuthenticatorDllPath                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ expandir \_ SZ                                                                                               |
| Descripción    | La ruta de acceso al archivo DLL del método de autenticación EAP. Por ejemplo,% SystemRoot% \\ system32 \\ &lt; nombre \_ de \_ dll &gt; . dll. |



 

## <a name="authenticatorfriendlyname"></a>AuthenticatorFriendlyName



| Valor constante | AuthenticatorFriendlyName                                                          |
|----------------|------------------------------------------------------------------------------------|
| Tipo           | Registro \_ SZ                                                                            |
| Descripción    | Cadena que contiene el nombre descriptivo (para mostrar) del método de autenticación de EAP. |



 

## <a name="configclsid"></a>ConfigCLSID



| Valor constante | ConfigCLSID                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | Registro \_ SZ                                                                                                                               |
| Descripción    | Cadena que contiene el GUID de la clase de configuración para este método de autenticación, con el formato {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} |



 

## <a name="properties"></a>Propiedades



| Valor constante | Propiedades                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | \_valor DWORD reg                                                                                                                                                  |
| Descripción    | Los bits de la DWORD se establecen para indicar la compatibilidad con la propiedad. Para obtener una lista de valores admitidos, consulte [**propiedades del método EAP**](eap-method-properties.md). |



 

## <a name="standalonesupported"></a>StandaloneSupported



| Valor constante | StandaloneSupported                                             |
|----------------|-----------------------------------------------------------------|
| Tipo           | \_valor DWORD reg                                                      |
| Descripción    | 0 si se trata de un método de autenticación independiente; 1 si no lo está. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Claves del registro del método EAP del mismo nivel](eap-peer-method-registry-keys.md)
</dt> <dt>

[Configuración del registro para tipos de EAP expandidos](registry-keys-for-eap-methods.md)
</dt> <dt>

[Uso de EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




