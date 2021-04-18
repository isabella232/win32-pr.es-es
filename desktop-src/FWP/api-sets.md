---
title: API DE WFP
description: La API de la plataforma de filtrado de Windows (WFP) se divide en los siguientes componentes.
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4230c82105f85c36e6fb112508a7128758b2ad60
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "105685808"
---
# <a name="wfp-api"></a>API DE WFP

La API de la plataforma de filtrado de Windows (WFP) se divide en los siguientes componentes.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente</th>
<th>Descripción</th>
<th>Archivos de encabezado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><a href="/windows-hardware/drivers/ddi/_netvista/">CALLOUT API</a> (FWPS) $ {Remove} $<br />
</td>
<td><a href="/windows-hardware/drivers/ddi/_netvista/">Tipos de datos</a> usados por las llamadas. <strong>Nota:</strong>  Estos tipos de datos se documentan en el kit de desarrollo de controladores (DDK) de Microsoft Windows.<br/></td>
<td><dl> fwpstypes. h<br />
fwpstypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows-hardware/drivers/ddi/_netvista/">Funciones</a> y <a href="/windows-hardware/drivers/ddi/_netvista/">tipos enumerados</a> que se usan para implementar llamadas. <strong>Nota:</strong>  Estas funciones y tipos enumerados se documentan en el DDK.<br/></td>
<td><dl> fwpsu. h<br />
fwpsk. h<br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2">API de IKE/AuthIP (IKEEXT) $ {REMOVE} $<br />
</td>
<td>Tipos y <a href="fwp-structs.md">estructuras</a> <a href="fwp-enums.md">enumerados</a> utilizados para administrar las asociaciones de seguridad y directivas de modo principal de IKE y AuthIP (mm).</td>
<td><dl> iketypes. h<br />
iketypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="fwp-ike-functions.md">Funciones</a> que se usan para administrar las asociaciones de seguridad y directivas de IKE y AuthIP mm.</td>
<td><dl> fwpmu. h<br />
fwpmk. h<br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2">IPsec API (IPSEC) $ {REMOVE} $<br />
</td>
<td>Tipos y <a href="fwp-structs.md">estructuras</a> <a href="fwp-enums.md">enumerados</a> utilizados para administrar directivas IPSec y asociaciones de seguridad.</td>
<td><dl> ipsectypes. h<br />
ipsectypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="fwp-ipsec-functions.md">Funciones</a> que se usan para administrar directivas IPSec y asociaciones de seguridad.</td>
<td><dl> fwpmu. h<br />
fwpmk. h<br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2">API de administración (FWPM) $ {REMOVE} $<br />
</td>
<td><a href="fwp-enums.md">Tipos enumerados</a> y <a href="fwp-structs.md">estructuras</a> que se usan para administrar el motor de filtro.</td>
<td><dl> fwpmtypes. h<br />
fwpmtypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="fwp-mgmt-functions.md">Funciones</a> utilizadas para administrar el motor de filtro. Estas funciones se utilizan para realizar las siguientes tareas:<br/>
<ul>
<li>Establecer y consultar filtros, proveedores y llamadas.</li>
<li>Recuperar estadísticas de IPsec.</li>
<li>Configure la plataforma de filtrado de Windows.</li>
</ul></td>
<td><dl> fwpmu. h<br />
fwpmk. h<br />
</dl></td>

</tr>
<tr class="odd">
<td>API compartida (FWP)</td>
<td>Tipos y <a href="fwp-structs.md">estructuras</a> fundamentales <a href="fwp-enums.md">enumerados</a> compartidos por la plataforma de filtrado de Windows.</td>
<td><dl> fwptypes. h<br />
fwptypes. idl<br />
</dl></td>
</tr>
</tbody>
</table>



 

Los nombres de los tipos de datos se encuentran en mayúsculas y con un carácter de subrayado. El nombre siempre comienza con un prefijo que identifica su grupo de componentes, como [**FWPM \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).

Los nombres de función se mezclan en mayúsculas y minúsculas. El nombre siempre comienza con un prefijo que identifica su grupo de componentes, como [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).

La mayoría de los nombres de datos y de funciones terminan con un número de versión. El archivo de encabezado fwpvi. h asigna los nombres de función y datos independientes de la versión a la versión que es adecuada para su uso con un sistema operativo determinado. Para obtener más información, consulte [los nombres de Version-Independent de WFP y el destino de versiones específicas de Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).

Cada componente no es independiente. Por ejemplo, las directivas de modo principal IKE (MM) se definen en el componente IKEEXT, pero se almacenan en un contexto de proveedor y se asocian con un filtro que se encuentran en el componente de la API FWPM.

## <a name="user-mode-and-kernel-mode-public-header-files"></a>User-Mode y Kernel-Mode archivos de encabezado públicos

La mayoría de las funciones de WFP se pueden llamar desde el modo de usuario o el modo kernel. Sin embargo, las funciones de modo de usuario devuelven un valor **DWORD** que representa un código de error de Win32, mientras que las funciones de modo kernel devuelven un valor de **NTSTATUS** que representa un código de estado de NT. Como resultado, los nombres de función y la semántica son idénticos entre el modo de usuario y el modo kernel, pero no las signaturas de función. Esto requiere encabezados específicos en modo de usuario y en modo kernel para los prototipos de función. Los nombres de archivo de encabezado de modo de usuario terminan en "u" y los nombres de archivo de encabezado de modo kernel terminan en "k".

En la tabla siguiente se enumeran los archivos de encabezado Win32 que definen las funciones de WFP.

| Archivos de encabezado | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fwpmk. h      | Prototipos de función de modo kernel para los componentes FWPM, IPsec y IKEEXT. Solo está disponible en el DDK.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| fwpmu. h      | Prototipos de función de modo de usuario para los componentes FWPM, IPsec y IKEEXT. Solo disponible en el kit de desarrollo de software (SDK) de Microsoft Windows.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| fwpsk. h      | Prototipos de función de modo kernel y tipos enumerados para el componente FWPS. Solo está disponible en el DDK.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| fwpsu. h      | Prototipos de función de modo de usuario y tipos enumerados para el componente FWPS. Solo está disponible en el Windows SDK. **Nota:**  Los tipos enumerados de modo de usuario FWPS son idénticos a los tipos enumerados de FWPS de modo kernel. En consecuencia, estos tipos se documentan solo en el DDK.<br/> **Nota:**  Los prototipos de función FWPS de modo usuario son idénticos a los prototipos de función FWPS de modo kernel con la excepción del código de retorno. Las funciones FWPS de modo usuario devuelven un **valor DWORD**, mientras que las funciones FWPS de modo kernel devuelven un **NTSTATUS**. En consecuencia, estas funciones solo se documentan en el DDK.<br/> |



 

Todas las funciones de modo de usuario se exportan desde fwpuclnt.dll. Todas las funciones de modo kernel se exportan desde fwpkclnt.sys.

### <a name="management-fwpm-and-callout-fwps-data-types"></a>Tipos de datos Management (FWPM) y Callout (FWPS)

La mayoría de los tipos de datos FWPM, que se usan para tareas de administración como agregar filtros o llamadas desde una aplicación o un controlador, tienen homólogos FWPS. Los tipos de datos FWPS se usan durante el filtrado real del tráfico de red, en el contexto de una rutina de llamada para la clasificación.

Por ejemplo, para agregar un filtro a una capa determinada del motor de filtrado, el programador debe usar un tipo FWPM, como: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET` . Para comprobar a qué capa se llama una llamada, el programador debe usar el tipo de FWPS correspondiente: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)` .

Algunos homólogos de FWPS para tipos de datos de FWPM están expandiendo los tipos de datos FWPM originales. Por ejemplo, para agregar una condición de filtro en muchas capas del motor de filtrado, el programador especifica `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` independientemente de la capa del motor de filtrado. Para buscar un valor de condición de filtro, el programador especifica un tipo de FWPS específico de la capa, como: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]` .

Los tipos de datos FWPS suelen ser más pequeños que sus homólogos FWPM. Por ejemplo, los [**identificadores de nivel de filtrado de FWPM**](management-filtering-layer-identifiers-.md) son **GUID** s (16 bytes), mientras que los [identificadores de nivel de filtrado de FWPS](/windows-hardware/drivers/network/management-filtering-layer-identifiers) son **UINT16** (16 bits). El tamaño más pequeño de los tipos de datos FWPS mejora el rendimiento del sistema, ya que las comparaciones de enteros compensan las comparaciones de **GUID** para el tráfico en tiempo real. Además, la memoria del kernel se utiliza de forma eficaz, ya que todos los tipos de FWPS se usan en el kernel para administrar los filtros, mientras que los tipos de FWPM se almacenan en modo de usuario para administrar los distintos niveles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos de API de WFP](object-model.md)
</dt> <dt>

[Administración de objetos de API de WFP](object-management.md)
</dt> </dl>

