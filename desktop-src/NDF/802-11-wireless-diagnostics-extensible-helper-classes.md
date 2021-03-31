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
# <a name="80211-wireless-diagnostics-extensible-helper-classes"></a><span data-ttu-id="34aab-103">802,11 clases auxiliares extensibles de diagnóstico inalámbrico</span><span class="sxs-lookup"><span data-stu-id="34aab-103">802.11 Wireless Diagnostics Extensible Helper Classes</span></span>

<span data-ttu-id="34aab-104">La infraestructura integrada de diagnósticos inalámbricos tiene dos puntos de extensión.</span><span class="sxs-lookup"><span data-stu-id="34aab-104">The built-in wireless diagnostics infrastructure has two extension points.</span></span>

| <span data-ttu-id="34aab-105">Clase auxiliar primaria</span><span class="sxs-lookup"><span data-stu-id="34aab-105">Parent Helper Class</span></span>                                | <span data-ttu-id="34aab-106">Propósito</span><span class="sxs-lookup"><span data-stu-id="34aab-106">Purpose</span></span>                                                           |
|----------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="34aab-107">Clase auxiliar extensible de WiFi nativo revisado (RNWF)</span><span class="sxs-lookup"><span data-stu-id="34aab-107">Revised Native Wifi (RNWF) Extensible Helper Class</span></span> | <span data-ttu-id="34aab-108">Diagnostica problemas relacionados con las extensiones de conectividad 802,11.</span><span class="sxs-lookup"><span data-stu-id="34aab-108">Diagnoses issues related to 802.11 connectivity extensions.</span></span>       |
| <span data-ttu-id="34aab-109">Clase auxiliar extensible L2Security</span><span class="sxs-lookup"><span data-stu-id="34aab-109">L2Security Extensible Helper Class</span></span>                 | <span data-ttu-id="34aab-110">Diagnostica los problemas relacionados con las extensiones de protocolo de seguridad de nivel 2.</span><span class="sxs-lookup"><span data-stu-id="34aab-110">Diagnoses issues related to Layer 2 security protocol extensions.</span></span> |



 

> [!Note]  
> <span data-ttu-id="34aab-111">Una clase auxiliar de terceros debe registrarse en ambas clases auxiliares primarias para asegurarse de que se llama a la clase de terceros.</span><span class="sxs-lookup"><span data-stu-id="34aab-111">A third-party helper class should register with both parent helper classes to ensure that the third-party class gets called.</span></span> <span data-ttu-id="34aab-112">Para obtener más información sobre el registro, vea [registrar extensiones de clase auxiliares de NDF](registering-ndf-helper-class-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="34aab-112">For more information about registration, see [Registering NDF Helper Class Extensions](registering-ndf-helper-class-extensions.md).</span></span>

 

## <a name="rnwf-extensible-helper-class"></a><span data-ttu-id="34aab-113">Clase auxiliar extensible RNWF</span><span class="sxs-lookup"><span data-stu-id="34aab-113">RNWF Extensible Helper Class</span></span>

<span data-ttu-id="34aab-114">Nombre de clase auxiliar principal</span><span class="sxs-lookup"><span data-stu-id="34aab-114">Parent Helper Class Name</span></span>

``` syntax
Parent = L"RNWF Extensible Helper Class";
```

<span data-ttu-id="34aab-115">La clase auxiliar extensible de Wi-Fi nativa revisada (RNWF) es la principal de las clases auxiliares de terceros que diagnostican problemas relacionados con la extensión de los protocolos 802,11 usados por Wi-Fi nativo.</span><span class="sxs-lookup"><span data-stu-id="34aab-115">The Revised Native Wifi (RNWF) extensible helper class is the parent for third-party helper classes that diagnose issues related to extending 802.11 protocols used by Native Wifi.</span></span>

<span data-ttu-id="34aab-116">Los dos atributos clave proporcionados por la clase auxiliar RNWF son el GUID de la interfaz donde se produjo el problema y el contexto de conexión.</span><span class="sxs-lookup"><span data-stu-id="34aab-116">The two key attributes provided by the RNWF helper class are the GUID of the interface where the issue occurred, and the connection context.</span></span>

-   <span data-ttu-id="34aab-117">GUID de la interfaz: este atributo se denomina "interface ID" y es de tipo **en \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="34aab-117">Interface GUID: This attribute is named "Interface ID" and is of type **AT\_GUID**.</span></span>

-   <span data-ttu-id="34aab-118">Contexto de conexión: este atributo se denomina ID. de red y es del tipo en la \_ cadena de octeto \_ .</span><span class="sxs-lookup"><span data-stu-id="34aab-118">Connection Context: This attribute is named Network ID and is of type AT\_OCTET\_STRING.</span></span> <span data-ttu-id="34aab-119">En realidad, esta cadena es un búfer de la \_ \_ estructura de identificador de WLAN WDIAG IHV \_ definida en Wlanihv. h.</span><span class="sxs-lookup"><span data-stu-id="34aab-119">This string is actually a buffer the WDIAG\_IHV\_WLAN\_ID structure defined in Wlanihv.h.</span></span> <span data-ttu-id="34aab-120">Esta estructura se define de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="34aab-120">This structure is defined as follows.</span></span>

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
> <span data-ttu-id="34aab-121">**WDIAG \_ La \_ seguridad del indicador de identificador de WLAN de IHV \_ \_ \_ \_ habilitada** es el único valor de **dwFlags** posible.</span><span class="sxs-lookup"><span data-stu-id="34aab-121">**WDIAG\_IHV\_WLAN\_ID\_FLAG\_SECURITY\_ENABLED** is the only possible **dwFlags** value.</span></span>

 

<span data-ttu-id="34aab-122">El atributo coincidente de la clase auxiliar de terceros debe ser el mismo que el identificador de servicio del módulo de software correspondiente.</span><span class="sxs-lookup"><span data-stu-id="34aab-122">The matching attribute for the third-party helper class should be the same as its corresponding software module's service ID.</span></span> <span data-ttu-id="34aab-123">También es el mismo nombre que el tercero debe estar registrado en el registro.</span><span class="sxs-lookup"><span data-stu-id="34aab-123">This is also the same name the third-party should be registered in the registry.</span></span> <span data-ttu-id="34aab-124">Diagnósticos inalámbricos consultará el identificador de servicio durante la sesión inalámbrica en la que se produjo el problema.</span><span class="sxs-lookup"><span data-stu-id="34aab-124">Wireless diagnostics will query the service ID during the wireless session in which the issue occurred.</span></span> <span data-ttu-id="34aab-125">La información se devolverá a NDF, que determinará si la clase auxiliar de terceros está presente y registrada y, a continuación, la llama.</span><span class="sxs-lookup"><span data-stu-id="34aab-125">The information will be returned to NDF, which will determine whether the third-party helper class is present and registered, and then call it.</span></span>

<span data-ttu-id="34aab-126">En la tabla siguiente se enumeran los atributos coincidentes de la clase auxiliar extensible RNWF.</span><span class="sxs-lookup"><span data-stu-id="34aab-126">The following table lists the matching attributes for the RNWF extensible helper class.</span></span>



| <span data-ttu-id="34aab-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="34aab-127">Name</span></span>          | <span data-ttu-id="34aab-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="34aab-128">Type</span></span>    | <span data-ttu-id="34aab-129">Value</span><span class="sxs-lookup"><span data-stu-id="34aab-129">Value</span></span>                         |
|---------------|---------|-------------------------------|
| <span data-ttu-id="34aab-130">DiagnosticsID</span><span class="sxs-lookup"><span data-stu-id="34aab-130">DiagnosticsID</span></span> | <span data-ttu-id="34aab-131">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="34aab-131">REG\_SZ</span></span> | <span data-ttu-id="34aab-132">\[DiagnosticsID \_ \_ cadena GUID</span><span class="sxs-lookup"><span data-stu-id="34aab-132">\[DiagnosticsID\_GUID\_String</span></span> |



 

## <a name="l2security-extensible-helper-class"></a><span data-ttu-id="34aab-133">Clase auxiliar extensible L2Security</span><span class="sxs-lookup"><span data-stu-id="34aab-133">L2Security Extensible Helper Class</span></span>

<span data-ttu-id="34aab-134">Nombre de clase auxiliar principal</span><span class="sxs-lookup"><span data-stu-id="34aab-134">Parent Helper Class Name</span></span>

``` syntax
Parent = L"Extensible L2Sec Helper Class";
```

<span data-ttu-id="34aab-135">La clase auxiliar extensible de seguridad de nivel 2 (L2Security) es la principal de las clases auxiliares de terceros que diagnostican problemas relacionados con los servicios y módulos de software correspondientes que reemplazan la funcionalidad de seguridad de capa 2.</span><span class="sxs-lookup"><span data-stu-id="34aab-135">The Layer 2 Security (L2Security) extensible helper class is the parent for third-party helper classes that diagnose issues related to corresponding services and software modules that replace Layer 2 Security functionality.</span></span>

<span data-ttu-id="34aab-136">Los dos atributos clave proporcionados por la clase auxiliar de seguridad de capa 2 son el GUID de la interfaz donde se produjo el problema y el contexto de conexión.</span><span class="sxs-lookup"><span data-stu-id="34aab-136">The two key attributes provided by the Layer 2 Security helper class are the GUID of the interface where the issue occurred, and the connection context.</span></span>

-   <span data-ttu-id="34aab-137">GUID de la interfaz: este atributo se denomina "interface ID" y es de tipo **en \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="34aab-137">Interface GUID: This attribute is named "Interface ID" and is of type **AT\_GUID**.</span></span>

-   <span data-ttu-id="34aab-138">Contexto de conexión: este atributo se denomina ID. de red y es del tipo en la \_ cadena de octeto \_ .</span><span class="sxs-lookup"><span data-stu-id="34aab-138">Connection Context: This attribute is named Network ID and is of type AT\_OCTET\_STRING.</span></span> <span data-ttu-id="34aab-139">En realidad, esta cadena es un búfer de la \_ \_ estructura de identificador de WLAN WDIAG IHV \_ definida en wlanihv. h.</span><span class="sxs-lookup"><span data-stu-id="34aab-139">This string is actually a buffer the WDIAG\_IHV\_WLAN\_ID structure defined in wlanihv.h.</span></span> <span data-ttu-id="34aab-140">Esta estructura se define de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="34aab-140">This structure is defined as follows.</span></span>

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
> <span data-ttu-id="34aab-141">**WDIAG \_ La \_ seguridad del indicador de identificador de WLAN de IHV \_ \_ \_ \_ habilitada** es el único valor de **dwFlags** posible.</span><span class="sxs-lookup"><span data-stu-id="34aab-141">**WDIAG\_IHV\_WLAN\_ID\_FLAG\_SECURITY\_ENABLED** is the only possible **dwFlags** value.</span></span>

 

<span data-ttu-id="34aab-142">El atributo coincidente de la clase auxiliar de terceros debe ser el mismo que el identificador de servicio del módulo de software correspondiente.</span><span class="sxs-lookup"><span data-stu-id="34aab-142">The matching attribute for the third-party helper class should be the same as its corresponding software module's service ID.</span></span> <span data-ttu-id="34aab-143">También es el mismo nombre que el tercero debe estar registrado en el registro.</span><span class="sxs-lookup"><span data-stu-id="34aab-143">This is also the same name the third-party should be registered in the registry.</span></span> <span data-ttu-id="34aab-144">Diagnósticos inalámbricos consultará el identificador de servicio durante la sesión inalámbrica en la que se produjo el problema.</span><span class="sxs-lookup"><span data-stu-id="34aab-144">Wireless diagnostics will query the service ID during the wireless session in which the issue occurred.</span></span> <span data-ttu-id="34aab-145">La información se devolverá a NDF, que determinará si la clase auxiliar de terceros está presente y registrada y, a continuación, la llama.</span><span class="sxs-lookup"><span data-stu-id="34aab-145">The information will be returned to NDF, which will determine whether the third-party helper class is present and registered, and then call it.</span></span>

<span data-ttu-id="34aab-146">En la tabla siguiente se enumeran los atributos coincidentes para la clase auxiliar extensible de seguridad de capa 2.</span><span class="sxs-lookup"><span data-stu-id="34aab-146">The following table lists the matching attributes for the Layer 2 Security extensible helper class.</span></span>



| <span data-ttu-id="34aab-147">Nombre</span><span class="sxs-lookup"><span data-stu-id="34aab-147">Name</span></span>          | <span data-ttu-id="34aab-148">Tipo</span><span class="sxs-lookup"><span data-stu-id="34aab-148">Type</span></span>    | <span data-ttu-id="34aab-149">Value</span><span class="sxs-lookup"><span data-stu-id="34aab-149">Value</span></span>                         |
|---------------|---------|-------------------------------|
| <span data-ttu-id="34aab-150">DiagnosticsID</span><span class="sxs-lookup"><span data-stu-id="34aab-150">DiagnosticsID</span></span> | <span data-ttu-id="34aab-151">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="34aab-151">REG\_SZ</span></span> | <span data-ttu-id="34aab-152">\[DiagnosticsID \_ \_ cadena GUID</span><span class="sxs-lookup"><span data-stu-id="34aab-152">\[DiagnosticsID\_GUID\_String</span></span> |



 

## <a name="matching-attributes"></a><span data-ttu-id="34aab-153">Atributos coincidentes</span><span class="sxs-lookup"><span data-stu-id="34aab-153">Matching Attributes</span></span>

<span data-ttu-id="34aab-154">**DiagnosticsID**</span><span class="sxs-lookup"><span data-stu-id="34aab-154">**DiagnosticsID**</span></span>

<span data-ttu-id="34aab-155">802,11 el diagnóstico inalámbrico consultará el *DiagnosticsID* desde el servicio Wi-Fi nativo básico para averiguar si se ha instalado en la conexión cualquier extensión inalámbrica o módulo de seguridad de terceros.</span><span class="sxs-lookup"><span data-stu-id="34aab-155">802.11 Wireless Diagnostics will query the *DiagnosticsID* from the core Native Wifi service in order to find out if any third-party wireless extensions or security modules are installed and involved in the connection.</span></span> <span data-ttu-id="34aab-156">Los diagnósticos inalámbricos proporcionarán supuestos a estas clases auxiliares de terceros mediante *DiagnosticsID* como atributo coincidente.</span><span class="sxs-lookup"><span data-stu-id="34aab-156">Wireless Diagnostics will then provide hypotheses to these third-party helper classes using the *DiagnosticsID* as the matching attribute.</span></span> <span data-ttu-id="34aab-157">Cualquier clase de aplicación auxiliar de terceros debe incluirse en el paquete de controladores asociado e instalarse con él.</span><span class="sxs-lookup"><span data-stu-id="34aab-157">Any third-party helper classes should be included in and installed with the associated driver package.</span></span> <span data-ttu-id="34aab-158">El *DiagnosticsID* se definirá en el archivo INF del minipuerto como una clave del registro en la directiva [AddReg](https://msdn.microsoft.com/library/ms794514.aspx) .</span><span class="sxs-lookup"><span data-stu-id="34aab-158">The *DiagnosticsID* will be defined in the miniport INF file as a registry key in the [AddReg](https://msdn.microsoft.com/library/ms794514.aspx) directive.</span></span>

``` syntax
HKR,Ndi\IHVExtensions, DiagnosticsID,0, "<Diagnostics ID GUID>"
```

<span data-ttu-id="34aab-159">Esta clave define el identificador de la clase auxiliar inalámbrica para el módulo de software de terceros.</span><span class="sxs-lookup"><span data-stu-id="34aab-159">This key defines the ID of the wireless helper class for the third-party software module.</span></span> <span data-ttu-id="34aab-160">Esta clave es opcional para el marco de extensibilidad, pero es necesaria si la implementación incluye una clase auxiliar inalámbrica IHV que se conecta a NDF y puede diagnosticar problemas de conectividad relacionados con las extensiones de seguridad o inalámbricas de RNWF.</span><span class="sxs-lookup"><span data-stu-id="34aab-160">This key is optional for the extensibility framework, but it is needed if the implementation includes an IHV Wireless Helper Class that plugs into NDF and can diagnose connectivity problems related to the RNWF wireless or security extensions.</span></span> <span data-ttu-id="34aab-161">Las clases auxiliares de diagnóstico de WLAN de MS consultarán este identificador desde el servicio de configuración automática inalámbrica cuando se instalen los módulos IHV y proporcionarán este identificador como el atributo de referencia o de coincidencia a NDF durante una sesión de diagnóstico para que NDF pueda llamar a la clase de aplicación auxiliar inalámbrica de terceros adecuada cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="34aab-161">MS WLAN diagnostics helper classes will query this ID from the Wireless Auto Configuration Service when IHV modules are installed and will provide this ID as the reference or matching attribute to NDF during a diagnostics session so that NDF can call the appropriate third-party wireless helper class when necessary.</span></span>

<span data-ttu-id="34aab-162">**\[DiagnosticsID \_ \_ cadena GUID\]**</span><span class="sxs-lookup"><span data-stu-id="34aab-162">**\[DiagnosticsID\_GUID\_String\]**</span></span>

<span data-ttu-id="34aab-163">Este valor debe ser una cadena con todas las letras mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="34aab-163">This value must be a string of all uppercase letters.</span></span> <span data-ttu-id="34aab-164">Por ejemplo, "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".</span><span class="sxs-lookup"><span data-stu-id="34aab-164">For example, "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".</span></span>

## <a name="scope-of-80211-wireless-diagnostics-helper-classes"></a><span data-ttu-id="34aab-165">Ámbito de las clases auxiliares de diagnóstico inalámbrico 802,11</span><span class="sxs-lookup"><span data-stu-id="34aab-165">Scope of 802.11 Wireless Diagnostics Helper Classes</span></span>

<span data-ttu-id="34aab-166">802,11 las clases auxiliares de diagnóstico inalámbricos diagnostican actualmente problemas inalámbricos en las siguientes áreas.</span><span class="sxs-lookup"><span data-stu-id="34aab-166">802.11 wireless diagnostics helper classes currently diagnose wireless issues in the following areas.</span></span>

-   <span data-ttu-id="34aab-167">Los problemas de conectividad 802,11, entre los que se incluyen 802,11 Association, 802,11, la configuración de seguridad de 802,11 relativa a los estándares de 802,11 & protocolos admitidos de forma nativa en el sistema operativo y problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="34aab-167">Any 802.11 connectivity issues including 802.11 association, 802.11 authentication, 802.11 security settings related to 802.11 standards & protocols natively supported in the operating system, and performance issues.</span></span>
-   <span data-ttu-id="34aab-168">Problemas de seguridad de nivel 2 con respecto a las configuraciones de 802.1 x y los problemas relacionados con la autenticación de nivel 2 mediante métodos que se admiten de forma nativa en Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="34aab-168">Layer 2 Security issues with regards to 802.1x configurations and any issues related to layer 2 authentication using methods natively supported on Windows Vista and Windows Server 2008.</span></span>
-   <span data-ttu-id="34aab-169">La configuración no coincide con la configuración de perfil entre el cliente y el punto de acceso, y los servicios y la infraestructura de red.</span><span class="sxs-lookup"><span data-stu-id="34aab-169">Configuration mismatches in profile settings between the client and the Access Point or the network infrastructure and services.</span></span>

<span data-ttu-id="34aab-170">las clases auxiliares de diagnóstico inalámbrico 802,11 no diagnostican problemas inalámbricos en las siguientes áreas.</span><span class="sxs-lookup"><span data-stu-id="34aab-170">802.11 wireless diagnostics helper classes currently do not diagnose wireless issues in the following areas.</span></span>

-   <span data-ttu-id="34aab-171">Problemas relacionados con las extensiones de terceros 802,11, incluido cualquier configuración de perfil o controlador relacionada con estas extensiones.</span><span class="sxs-lookup"><span data-stu-id="34aab-171">Issues related to third-party 802.11 extensions including any profile or driver settings related to these extensions.</span></span>
-   <span data-ttu-id="34aab-172">Problemas relacionados con métodos EAP de terceros.</span><span class="sxs-lookup"><span data-stu-id="34aab-172">Issues related to third-party EAP methods.</span></span>
-   <span data-ttu-id="34aab-173">Problemas con el controlador de minipuerto inalámbrico.</span><span class="sxs-lookup"><span data-stu-id="34aab-173">Wireless miniport driver issues.</span></span>
-   <span data-ttu-id="34aab-174">Cualquier problema relacionado con los estándares y el protocolo de seguridad 802,11 y nivel 2 que no se admiten de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="34aab-174">Any 802.11 and layer 2 security protocol or standards-related issues that are not natively supported.</span></span>
-   <span data-ttu-id="34aab-175">Problemas de nivel de componente o del sistema que podrían afectar a la conectividad inalámbrica, como la administración de energía, el poco espacio en disco, las condiciones de memoria y los problemas de hardware.</span><span class="sxs-lookup"><span data-stu-id="34aab-175">System or component-level issues that might impact wireless connectivity, such as power management, low disk space, memory conditions, and hardware problems.</span></span>

<span data-ttu-id="34aab-176">Además, el diagnóstico inalámbrico 802,11 no analiza los casos de [**HighUtilization**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) .</span><span class="sxs-lookup"><span data-stu-id="34aab-176">Additionally, 802.11 Wireless Diagnostics does not analyze [**HighUtilization**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) cases.</span></span> <span data-ttu-id="34aab-177">Los problemas de rendimiento inalámbrico identificados se analizarán y se indicarán como casos de [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) .</span><span class="sxs-lookup"><span data-stu-id="34aab-177">Identified wireless performance issues will be analyzed and reported as [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) cases.</span></span>

 

 




