---
title: 802.11 Clases auxiliares extensibles de diagnóstico inalámbrico
description: La infraestructura de diagnóstico inalámbrica integrada tiene dos puntos de extensión. Clase auxiliar primariaPurposeRevised Native Wifi (RNWF) Clase auxiliar extensibleDiagnoses problemas relacionados con las extensiones de conectividad 802.11.
ms.assetid: b54f836d-4fae-4e71-bf7b-af5a6e9e615c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde49561c68044157c9d518571b8241c49dcf25
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161229"
---
# <a name="80211-wireless-diagnostics-extensible-helper-classes"></a>802.11 Clases auxiliares extensibles de diagnóstico inalámbrico

La infraestructura de diagnóstico inalámbrica integrada tiene dos puntos de extensión.

| Clase auxiliar primaria                                | Propósito                                                           |
|----------------------------------------------------|-------------------------------------------------------------------|
| Revised Native Wifi (RNWF) Extensible Helper Class | Diagnostica problemas relacionados con las extensiones de conectividad 802.11.       |
| L2Security Extensible Helper Class                 | Diagnostica problemas relacionados con las extensiones del protocolo de seguridad de nivel 2. |



 

> [!Note]  
> Una clase auxiliar de terceros debe registrarse con ambas clases auxiliares primarias para asegurarse de que se llama a la clase de terceros. Para obtener más información sobre el registro, vea [Registering NDF Helper Class Extensions](registering-ndf-helper-class-extensions.md).

 

## <a name="rnwf-extensible-helper-class"></a>RNWF Extensible Helper (clase auxiliar)

Nombre de clase del asistente primario

``` syntax
Parent = L"RNWF Extensible Helper Class";
```

La clase auxiliar extensible Revised Native Wifi (RNWF) es la principal para las clases auxiliares de terceros que diagnostican problemas relacionados con la extensión de los protocolos 802.11 usados por Native Wifi.

Los dos atributos clave proporcionados por la clase auxiliar RNWF son el GUID de la interfaz donde se produjo el problema y el contexto de conexión.

-   GUID de interfaz: este atributo se denomina "Id. de interfaz" y es de tipo **AT \_ GUID**.

-   Contexto de conexión: este atributo se denomina Id. de red y es de tipo AT \_ OCTET \_ STRING. Esta cadena es realmente un búfer de la estructura WDIAG \_ IHV \_ WLAN ID definida en \_ Wlanuyav.h. Esta estructura se define como se muestra a continuación.

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> **WDIAG \_ IHV \_ WLAN ID FLAG SECURITY \_ \_ \_ \_ ENABLED** es el único valor **dwFlags** posible.

 

El atributo correspondiente para la clase auxiliar de terceros debe ser el mismo que el identificador de servicio del módulo de software correspondiente. También es el mismo nombre que el tercero debe registrarse en el registro. Los diagnósticos inalámbricos consultarán el identificador de servicio durante la sesión inalámbrica en la que se produjo el problema. La información se devolverá a NDF, que determinará si la clase auxiliar de terceros está presente y registrada y, a continuación, la llamará.

En la tabla siguiente se enumeran los atributos correspondientes para la clase auxiliar extensible RNWF.



| Nombre          | Tipo    | Value                         |
|---------------|---------|-------------------------------|
| DiagnosticsID | REG \_ SZ | \[Cadena GUID de DiagnosticsID \_ \_ |



 

## <a name="l2security-extensible-helper-class"></a>L2Security Extensible Helper Class

Nombre de clase del asistente primario

``` syntax
Parent = L"Extensible L2Sec Helper Class";
```

La clase auxiliar extensible Seguridad de nivel 2 (L2Security) es la principal para las clases auxiliares de terceros que diagnostican problemas relacionados con los servicios y módulos de software correspondientes que reemplazan a la funcionalidad de seguridad de nivel 2.

Los dos atributos clave proporcionados por la clase auxiliar de seguridad de nivel 2 son el GUID de la interfaz donde se produjo el problema y el contexto de conexión.

-   GUID de interfaz: este atributo se denomina "Id. de interfaz" y es de tipo **AT \_ GUID**.

-   Contexto de conexión: este atributo se denomina Id. de red y es de tipo AT \_ OCTET \_ STRING. Esta cadena es realmente un búfer de la estructura WDIAG \_ IHV \_ WLAN ID definida en \_ wlanuyav.h. Esta estructura se define como se muestra a continuación.

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> **WDIAG \_ IHV \_ WLAN ID FLAG SECURITY \_ \_ \_ \_ ENABLED** es el único valor **dwFlags** posible.

 

El atributo correspondiente para la clase auxiliar de terceros debe ser el mismo que el identificador de servicio del módulo de software correspondiente. También es el mismo nombre que el tercero debe registrarse en el registro. Los diagnósticos inalámbricos consultarán el identificador de servicio durante la sesión inalámbrica en la que se produjo el problema. La información se devolverá a NDF, que determinará si la clase auxiliar de terceros está presente y registrada y, a continuación, la llamará.

En la tabla siguiente se enumeran los atributos correspondientes para la clase auxiliar extensible seguridad de capa 2.



| Nombre          | Tipo    | Value                         |
|---------------|---------|-------------------------------|
| DiagnosticsID | REG \_ SZ | \[Cadena GUID de DiagnosticsID \_ \_ |



 

## <a name="matching-attributes"></a>Atributos de coincidencia

**DiagnosticsID**

802.11 Diagnósticos inalámbricos consultará *diagnosticsID* desde el servicio Wi-Fi nativo principal para averiguar si hay extensiones inalámbricas de terceros o módulos de seguridad instalados e implicados en la conexión. A continuación, diagnósticos inalámbricos proporcionarán hipótesis a estas clases auxiliares de terceros mediante *DiagnosticsID* como atributo de coincidencia. Las clases auxiliares de terceros deben incluirse e instalarse con el paquete de controladores asociado. *DiagnosticsID se* definirá en el archivo INF de miniportador como una clave del Registro en la [directiva AddReg.](https://msdn.microsoft.com/library/ms794514.aspx)

``` syntax
HKR,Ndi\IHVExtensions, DiagnosticsID,0, "<Diagnostics ID GUID>"
```

Esta clave define el identificador de la clase auxiliar inalámbrica para el módulo de software de terceros. Esta clave es opcional para el marco de extensibilidad, pero es necesaria si la implementación incluye una clase auxiliar inalámbrica IHV que se conecta a NDF y puede diagnosticar problemas de conectividad relacionados con las extensiones inalámbricas o de seguridad RNWF. Las clases auxiliares de diagnóstico de MS WLAN consultarán este identificador desde el servicio de configuración automática inalámbrica cuando se instalen módulos IHV y proporcionarán este identificador como referencia o atributo correspondiente a NDF durante una sesión de diagnóstico para que NDF pueda llamar a la clase auxiliar inalámbrica de terceros adecuada cuando sea necesario.

**\[Cadena GUID de DiagnosticsID \_ \_\]**

Este valor debe ser una cadena de todas las letras mayúsculas. Por ejemplo, "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".

## <a name="scope-of-80211-wireless-diagnostics-helper-classes"></a>Ámbito de las clases auxiliares de diagnóstico inalámbrico 802.11

Las clases auxiliares de diagnóstico inalámbrico 802.11 actualmente diagnostican problemas inalámbricos en las áreas siguientes.

-   Cualquier problema de conectividad 802.11, incluida la asociación 802.11, la autenticación 802.11, la configuración de seguridad 802.11 relacionada con los estándares 802.11 & protocolos admitidos de forma nativa en el sistema operativo y problemas de rendimiento.
-   Problemas de seguridad de nivel 2 con respecto a las configuraciones 802.1x y cualquier problema relacionado con la autenticación de nivel 2 mediante los métodos admitidos de forma nativa en Windows Vista y Windows Server 2008.
-   La configuración no coincide en la configuración de perfil entre el cliente y el punto de acceso o la infraestructura de red y los servicios.

Actualmente, las clases auxiliares de diagnóstico inalámbrico 802.11 no diagnostican problemas inalámbricos en las áreas siguientes.

-   Problemas relacionados con las extensiones 802.11 de terceros, incluida cualquier configuración de perfil o controlador relacionada con estas extensiones.
-   Problemas relacionados con métodos EAP de terceros.
-   Problemas del controlador de minipuerto inalámbrico.
-   Cualquier protocolo de seguridad 802.11 y nivel 2 o problemas relacionados con los estándares que no se admiten de forma nativa.
-   Problemas de nivel de sistema o componente que podrían afectar a la conectividad inalámbrica, como la administración de energía, el poco espacio en disco, las condiciones de memoria y los problemas de hardware.

Además, 802.11 Diagnóstico inalámbrico no analiza los [**casos de HighUtilization.**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) Los problemas de rendimiento inalámbrico identificados se analizarán y se notifican [**como casos lowhealth.**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth)

 

 




