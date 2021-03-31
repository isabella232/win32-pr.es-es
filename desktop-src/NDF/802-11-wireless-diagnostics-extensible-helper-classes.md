---
title: 802,11 clases auxiliares extensibles de diagnóstico inalámbrico
description: La infraestructura integrada de diagnósticos inalámbricos tiene dos puntos de extensión. Ayudante primario ClassPurposeRevised aplicación auxiliar extensible Wi-Fi (RNWF) Complementos de ClassDiagnosess relacionados con las extensiones de conectividad 802,11.
ms.assetid: b54f836d-4fae-4e71-bf7b-af5a6e9e615c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde49561c68044157c9d518571b8241c49dcf25
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104533016"
---
# <a name="80211-wireless-diagnostics-extensible-helper-classes"></a>802,11 clases auxiliares extensibles de diagnóstico inalámbrico

La infraestructura integrada de diagnósticos inalámbricos tiene dos puntos de extensión.

| Clase auxiliar primaria                                | Propósito                                                           |
|----------------------------------------------------|-------------------------------------------------------------------|
| Clase auxiliar extensible de WiFi nativo revisado (RNWF) | Diagnostica problemas relacionados con las extensiones de conectividad 802,11.       |
| Clase auxiliar extensible L2Security                 | Diagnostica los problemas relacionados con las extensiones de protocolo de seguridad de nivel 2. |



 

> [!Note]  
> Una clase auxiliar de terceros debe registrarse en ambas clases auxiliares primarias para asegurarse de que se llama a la clase de terceros. Para obtener más información sobre el registro, vea [registrar extensiones de clase auxiliares de NDF](registering-ndf-helper-class-extensions.md).

 

## <a name="rnwf-extensible-helper-class"></a>Clase auxiliar extensible RNWF

Nombre de clase auxiliar principal

``` syntax
Parent = L"RNWF Extensible Helper Class";
```

La clase auxiliar extensible de Wi-Fi nativa revisada (RNWF) es la principal de las clases auxiliares de terceros que diagnostican problemas relacionados con la extensión de los protocolos 802,11 usados por Wi-Fi nativo.

Los dos atributos clave proporcionados por la clase auxiliar RNWF son el GUID de la interfaz donde se produjo el problema y el contexto de conexión.

-   GUID de la interfaz: este atributo se denomina "interface ID" y es de tipo **en \_ GUID**.

-   Contexto de conexión: este atributo se denomina ID. de red y es del tipo en la \_ cadena de octeto \_ . En realidad, esta cadena es un búfer de la \_ \_ estructura de identificador de WLAN WDIAG IHV \_ definida en Wlanihv. h. Esta estructura se define de la siguiente manera.

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
> **WDIAG \_ La \_ seguridad del indicador de identificador de WLAN de IHV \_ \_ \_ \_ habilitada** es el único valor de **dwFlags** posible.

 

El atributo coincidente de la clase auxiliar de terceros debe ser el mismo que el identificador de servicio del módulo de software correspondiente. También es el mismo nombre que el tercero debe estar registrado en el registro. Diagnósticos inalámbricos consultará el identificador de servicio durante la sesión inalámbrica en la que se produjo el problema. La información se devolverá a NDF, que determinará si la clase auxiliar de terceros está presente y registrada y, a continuación, la llama.

En la tabla siguiente se enumeran los atributos coincidentes de la clase auxiliar extensible RNWF.



| Nombre          | Tipo    | Value                         |
|---------------|---------|-------------------------------|
| DiagnosticsID | Registro \_ SZ | \[DiagnosticsID \_ \_ cadena GUID |



 

## <a name="l2security-extensible-helper-class"></a>Clase auxiliar extensible L2Security

Nombre de clase auxiliar principal

``` syntax
Parent = L"Extensible L2Sec Helper Class";
```

La clase auxiliar extensible de seguridad de nivel 2 (L2Security) es la principal de las clases auxiliares de terceros que diagnostican problemas relacionados con los servicios y módulos de software correspondientes que reemplazan la funcionalidad de seguridad de capa 2.

Los dos atributos clave proporcionados por la clase auxiliar de seguridad de capa 2 son el GUID de la interfaz donde se produjo el problema y el contexto de conexión.

-   GUID de la interfaz: este atributo se denomina "interface ID" y es de tipo **en \_ GUID**.

-   Contexto de conexión: este atributo se denomina ID. de red y es del tipo en la \_ cadena de octeto \_ . En realidad, esta cadena es un búfer de la \_ \_ estructura de identificador de WLAN WDIAG IHV \_ definida en wlanihv. h. Esta estructura se define de la siguiente manera.

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
> **WDIAG \_ La \_ seguridad del indicador de identificador de WLAN de IHV \_ \_ \_ \_ habilitada** es el único valor de **dwFlags** posible.

 

El atributo coincidente de la clase auxiliar de terceros debe ser el mismo que el identificador de servicio del módulo de software correspondiente. También es el mismo nombre que el tercero debe estar registrado en el registro. Diagnósticos inalámbricos consultará el identificador de servicio durante la sesión inalámbrica en la que se produjo el problema. La información se devolverá a NDF, que determinará si la clase auxiliar de terceros está presente y registrada y, a continuación, la llama.

En la tabla siguiente se enumeran los atributos coincidentes para la clase auxiliar extensible de seguridad de capa 2.



| Nombre          | Tipo    | Value                         |
|---------------|---------|-------------------------------|
| DiagnosticsID | Registro \_ SZ | \[DiagnosticsID \_ \_ cadena GUID |



 

## <a name="matching-attributes"></a>Atributos coincidentes

**DiagnosticsID**

802,11 el diagnóstico inalámbrico consultará el *DiagnosticsID* desde el servicio Wi-Fi nativo básico para averiguar si se ha instalado en la conexión cualquier extensión inalámbrica o módulo de seguridad de terceros. Los diagnósticos inalámbricos proporcionarán supuestos a estas clases auxiliares de terceros mediante *DiagnosticsID* como atributo coincidente. Cualquier clase de aplicación auxiliar de terceros debe incluirse en el paquete de controladores asociado e instalarse con él. El *DiagnosticsID* se definirá en el archivo INF del minipuerto como una clave del registro en la directiva [AddReg](https://msdn.microsoft.com/library/ms794514.aspx) .

``` syntax
HKR,Ndi\IHVExtensions, DiagnosticsID,0, "<Diagnostics ID GUID>"
```

Esta clave define el identificador de la clase auxiliar inalámbrica para el módulo de software de terceros. Esta clave es opcional para el marco de extensibilidad, pero es necesaria si la implementación incluye una clase auxiliar inalámbrica IHV que se conecta a NDF y puede diagnosticar problemas de conectividad relacionados con las extensiones de seguridad o inalámbricas de RNWF. Las clases auxiliares de diagnóstico de WLAN de MS consultarán este identificador desde el servicio de configuración automática inalámbrica cuando se instalen los módulos IHV y proporcionarán este identificador como el atributo de referencia o de coincidencia a NDF durante una sesión de diagnóstico para que NDF pueda llamar a la clase de aplicación auxiliar inalámbrica de terceros adecuada cuando sea necesario.

**\[DiagnosticsID \_ \_ cadena GUID\]**

Este valor debe ser una cadena con todas las letras mayúsculas. Por ejemplo, "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".

## <a name="scope-of-80211-wireless-diagnostics-helper-classes"></a>Ámbito de las clases auxiliares de diagnóstico inalámbrico 802,11

802,11 las clases auxiliares de diagnóstico inalámbricos diagnostican actualmente problemas inalámbricos en las siguientes áreas.

-   Los problemas de conectividad 802,11, entre los que se incluyen 802,11 Association, 802,11, la configuración de seguridad de 802,11 relativa a los estándares de 802,11 & protocolos admitidos de forma nativa en el sistema operativo y problemas de rendimiento.
-   Problemas de seguridad de nivel 2 con respecto a las configuraciones de 802.1 x y los problemas relacionados con la autenticación de nivel 2 mediante métodos que se admiten de forma nativa en Windows Vista y Windows Server 2008.
-   La configuración no coincide con la configuración de perfil entre el cliente y el punto de acceso, y los servicios y la infraestructura de red.

las clases auxiliares de diagnóstico inalámbrico 802,11 no diagnostican problemas inalámbricos en las siguientes áreas.

-   Problemas relacionados con las extensiones de terceros 802,11, incluido cualquier configuración de perfil o controlador relacionada con estas extensiones.
-   Problemas relacionados con métodos EAP de terceros.
-   Problemas con el controlador de minipuerto inalámbrico.
-   Cualquier problema relacionado con los estándares y el protocolo de seguridad 802,11 y nivel 2 que no se admiten de forma nativa.
-   Problemas de nivel de componente o del sistema que podrían afectar a la conectividad inalámbrica, como la administración de energía, el poco espacio en disco, las condiciones de memoria y los problemas de hardware.

Además, el diagnóstico inalámbrico 802,11 no analiza los casos de [**HighUtilization**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) . Los problemas de rendimiento inalámbrico identificados se analizarán y se indicarán como casos de [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) .

 

 




