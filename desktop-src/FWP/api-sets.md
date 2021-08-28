---
title: WFP API
description: La API Windows Filtering Platform (WFP) se divide en los siguientes componentes.
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eadbb3fb6383999b2bb8ef14c99ecb8beab3f88
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470152"
---
# <a name="wfp-api"></a>WFP API

La API Windows Filtering Platform (WFP) se divide en los siguientes componentes.




| Componente | Descripción | Archivos de encabezado | 
|-----------|-------------|--------------|
| <a href="/windows-hardware/drivers/ddi/_netvista/">API de llamada</a> (FWPS)${REMOVE}$<br /> | <a href="/windows-hardware/drivers/ddi/_netvista/">Tipos de datos</a> utilizados por las llamadas. <strong>Nota</strong>  Estos tipos de datos se documentan en Microsoft Windows Driver Development Kit (DDK).<br /> | <dl> fwpstypes.h<br />fwpstypes.idl<br /></dl> | 
| <a href="/windows-hardware/drivers/ddi/_netvista/">Funciones</a> y <a href="/windows-hardware/drivers/ddi/_netvista/">tipos enumerados que</a> se usan para implementar llamadas. <strong>Nota</strong>  Estas funciones y tipos enumerados se documentan en el DDK.<br /> | <dl> fwpsu.h<br />fwpsk.h<br /></dl> | 
| IKE/AuthIP API (IXTXT)${REMOVE}$<br /> | <a href="fwp-enums.md">Tipos y estructuras enumerados</a> <a href="fwp-structs.md">que se</a> usan para administrar las asociaciones de seguridad y directivas de modo principal (MM) de IKE y AuthIP. | <dl> iketypes.h<br />iketypes.idl<br /></dl> | 
| <a href="fwp-ike-functions.md">Funciones</a> que se usan para administrar las asociaciones de seguridad y directivas de MM de IKE y AuthIP. | <dl> fwpmu.h<br />fwpmk.h<br /></dl> | 
| API de IPsec (IPSEC)${REMOVE}$<br /> | <a href="fwp-enums.md">Tipos y estructuras enumerados</a> <a href="fwp-structs.md">que se</a> usan para administrar las directivas de IPsec y las asociaciones de seguridad. | <dl> ipsectypes.h<br />ipsectypes.idl<br /></dl> | 
| <a href="fwp-ipsec-functions.md">Funciones que</a> se usan para administrar las directivas de IPsec y las asociaciones de seguridad. | <dl> fwpmu.h<br />fwpmk.h<br /></dl> | 
| API de Administración (FWPM)${REMOVE}$<br /> | <a href="fwp-enums.md">Tipos y estructuras enumerados</a> <a href="fwp-structs.md">que se</a> usan para administrar el motor de filtros. | <dl> fwpmtypes.h<br />fwpmtypes.idl<br /></dl> | 
| <a href="fwp-mgmt-functions.md">Funciones</a> usadas para administrar el motor de filtros. Estas funciones se usan para realizar las siguientes tareas:<br /><ul><li>Establezca y consulte filtros, proveedores y llamadas.</li><li>Recuperar estadísticas de IPsec.</li><li>Configure la plataforma Windows filtrado de datos.</li></ul> | <dl> fwpmu.h<br />fwpmk.h<br /></dl> | 
| API compartida (FWP) | Tipos <a href="fwp-enums.md">y estructuras enumerados</a> <a href="fwp-structs.md">fundamentales compartidos</a> en Windows plataforma de filtrado. | <dl> fwptypes.h<br />fwptypes.idl<br /></dl> | 




 

Los nombres de tipo de datos están todos en mayúsculas y con caracteres de subrayado delimitados. El nombre siempre comienza con un prefijo que identifica su grupo de componentes, como [**FWPM \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).

Los nombres de función están entre mayúsculas y minúsculas y están delimitados por mayúsculas y minúsculas. El nombre siempre comienza con un prefijo que identifica su grupo de componentes, como [**FwpmProviderContextAdd0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0)

La mayoría de los nombres de datos y funciones terminan con un número de versión. El archivo de encabezado fwpvi.h asigna los nombres de función y datos independientes de la versión a la versión adecuada para su uso con un sistema operativo determinado. Para obtener más información, vea [WFP Version-Independent nombres y versiones](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md)específicas de destino de Windows .

Cada componente no es independiente. Por ejemplo, las directivas de modo principal (MM) de IKE se definen en el componente IXTXT, pero se almacenan en un contexto de proveedor y están asociadas a un filtro que se encuentra en el componente de LA API FWPM.

## <a name="user-mode-and-kernel-mode-public-header-files"></a>User-Mode y Kernel-Mode archivos de encabezado públicos

La mayoría de las funciones WFP se pueden llamar desde el modo de usuario o el modo kernel. Sin embargo, las funciones en modo de usuario devuelven un valor **DWORD** que representa un código de error win32, mientras que las funciones en modo kernel devuelven un valor **NTSTATUS** que representa un código de estado NT. Como resultado, los nombres de función y la semántica son idénticos entre el modo de usuario y el modo kernel, pero las firmas de función no lo son. Esto requiere encabezados específicos de modo de usuario y modo kernel independientes para los prototipos de función. Los nombres de archivo de encabezado en modo de usuario terminan en "u" y los nombres de archivo de encabezado en modo kernel terminan en "k".

En la tabla siguiente se enumeran los archivos de encabezado de Win32 que definen las funciones WFP.

| Archivos de encabezado | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fwpmk.h      | Prototipos de funciones en modo kernel para los componentes FWPM, IPsec e IXTXT. Disponible solo en el DDK.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| fwpmu.h      | Prototipos de funciones en modo de usuario para los componentes FWPM, IPsec e IXTXT. Disponible solo en microsoft Windows Software Development Kit (SDK).                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| fwpsk.h      | Prototipos de funciones en modo kernel y tipos enumerados para el componente FWPS. Disponible solo en el DDK.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| fwpsu.h      | Prototipos de función en modo de usuario y tipos enumerados para el componente FWPS. Disponible solo en Windows SDK. **Nota**  Los tipos enumerados de FWPS en modo de usuario son idénticos a los tipos enumerados FWPS en modo kernel. En consecuencia, estos tipos solo se documentan en el DDK.<br/> **Nota**  Los prototipos de función FWPS en modo de usuario son idénticos a los prototipos de función FWPS en modo kernel con la excepción del código de retorno. Las funciones FWPS en modo de usuario devuelven **un DWORD,** mientras que las funciones FWPS en modo kernel devuelven **un NTSTATUS**. En consecuencia, estas funciones solo se documentan en el DDK.<br/> |



 

Todas las funciones en modo de usuario se exportan desde fwpuclnt.dll. Todas las funciones en modo kernel se exportan desde fwpkclnt.sys.

### <a name="management-fwpm-and-callout-fwps-data-types"></a>Tipos de datos management (FWPM) y callout (FWPS)

La mayoría de los tipos de datos FWPM, que se usan para tareas de administración como agregar filtros o llamadas desde una aplicación o controlador, tienen homólogos FWPS. Los tipos de datos FWPS se usan durante el filtrado real del tráfico de red, en el contexto de una rutina de llamada para la clasificación.

Por ejemplo, para agregar un filtro a una capa de motor de filtrado determinada, el programador debe usar un tipo FWPM, como: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET` . Para comprobar desde qué capa se llama a una llamada, el programador debe usar el tipo FWPS correspondiente: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)` .

Algunos homólogos de FWPS a los tipos de datos FWPM están expandiendo los tipos de datos FWPM originales. Por ejemplo, para agregar una condición de filtro en muchas capas del motor de filtrado, el programador especifica el , independientemente de la `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` capa del motor de filtrado. Para buscar un valor de condición de filtro, el programador especifica un tipo FWPS específico de la capa, como: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]` .

Los tipos de datos FWPS suelen ser menores que sus homólogos fwpm. Por ejemplo, los identificadores de capa de filtrado [**FWPM**](management-filtering-layer-identifiers-.md) son **GUID**(16 bytes), mientras que los identificadores de capa de filtrado [FWPS](/windows-hardware/drivers/network/management-filtering-layer-identifiers) son **UINT16** (16 bits). El tamaño más pequeño de los tipos de datos FWPS mejora el rendimiento del sistema, ya que las comparaciones de enteros superan a las comparaciones **DE GUID** para el tráfico en tiempo real. Además, la memoria del kernel se usa de forma eficaz, ya que todos los tipos FWPS se usan en el kernel para administrar los filtros, mientras que los tipos FWPM se almacenan en modo de usuario para administrar las distintas capas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos de LA API de WFP](object-model.md)
</dt> <dt>

[Administración de objetos de LA API de WFP](object-management.md)
</dt> </dl>

