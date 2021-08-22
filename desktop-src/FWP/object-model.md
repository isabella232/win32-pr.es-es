---
title: Modelo de objetos
description: En la tabla siguiente se enumeran los tipos de objeto que se pueden manipular a través de los distintos conjuntos de API proporcionados por Windows Filtering Platform (WFP).
ms.assetid: 6931583f-785c-4e27-b5e4-d185d23a54ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12acbb2ece5049a8c9bf19bb3796be88f4fed0fbba8d46d75b9d41e206522ce0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119255705"
---
# <a name="object-model"></a>Modelo de objetos

En la tabla siguiente se enumeran los tipos de objeto que se pueden manipular a través de los distintos conjuntos de API proporcionados por Windows Filtering Platform (WFP).



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de objeto</th>
<th>Descripción</th>
<th>Propiedades de ejemplo</th>
<th>Ejemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Filtrar</td>
<td>Regla que rige la clasificación. Si se cumplen las condiciones, se invoca la acción . <br/> Este es el objeto más complejo expuesto por WFP, ya que une todos los demás tipos de objeto. <br/></td>
<td><ul>
<li>Matriz de condiciones</li>
<li>Acción (Permitir, Bloquear, Llamada)</li>
<li><a href="filter-weight-assignment.md">Peso</a></li>
<li>Context</li>
</ul></td>
<td>&quot;Bloquee el tráfico con un puerto TCP mayor que 1024.&quot; <br/> &quot;Llamada a IDS para todo el tráfico que no está protegido.&quot;<br/></td>
</tr>
<tr class="even">
<td>Llamada</td>
<td>Conjunto de funciones que participan en el proceso de clasificación.<br/> Permite que el procesamiento de paquetes personalizados se haga cuando se cumplen ciertas condiciones.<br/></td>
<td><ul>
<li>ID</li>
<li>Capa aplicable</li>
</ul></td>
<td>El controlador NAT<br/></td>
</tr>
<tr class="odd">
<td>Nivel</td>
<td>Contenedor de filtros en el motor de filtros. <br/> Representa un punto específico en el procesamiento del tráfico de red donde se invoca el motor de filtro.<br/></td>
<td><ul>
<li>Esquema de los filtros que se pueden agregar a la capa</li>
</ul></td>
<td>La capa de transporte de entrada<br/></td>
</tr>
<tr class="even">
<td>Subcapa</td>
<td>Un sub-componente de una capa, que se usa en el <a href="filter-arbitration.md">arbitraje de filtro.</a><br/></td>
<td><ul>
<li>Peso</li>
</ul></td>
<td>Subcapa Tunnel IPsec<br/></td>
</tr>
<tr class="odd">
<td>Proveedor</td>
<td>Proveedor de directivas que ha creado una solución en WFP.<br/> Se usa únicamente para la administración; no afecta al procesamiento de paquetes en tiempo de ejecución.<br/></td>
<td><ul>
<li>ID</li>
<li>Nombre del servicio</li>
</ul></td>
<td>Firewall de Windows con seguridad avanzada<br/> Una aplicación de filtrado de direcciones URL de terceros<br/></td>
</tr>
<tr class="even">
<td>Contexto del proveedor</td>
<td>Blob de datos usado por un proveedor de directivas para almacenar información de contexto arbitraria. <br/> Se usa para pasar información de configuración personalizada a una llamada.<br/> La manera más común de usar la información de contexto es hacer que los filtros hacen referencia a un contexto de proveedor. <br/></td>
<td><ul>
<li>ID</li>
<li>Blob en datos</li>
</ul></td>
<td>IPsec almacena la configuración de autenticación en el motor de filtrado base (BFE). La &quot; propiedad Context de un filtro indica la configuración de &quot; autenticación que se usará para el tráfico que describe el filtro.<br/> La corrección de compatibilidad (shim) de la selección de certificación SSL almacenará la información de certificación en un contexto de proveedor. <br/></td>
</tr>
</tbody>
</table>



 

Los tipos de objeto expuestos por la API de WFP tienen una semántica coherente. Las acciones de agregar, enumerar, suscribir, y así sucesivamente son similares para todos los tipos de objeto.

Cada tipo de objeto se representa mediante una estructura de datos (por ejemplo, [**FWPM \_ FILTER0).**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0) Para minimizar el número de estructuras de datos diferentes expuestas por la API de WFP, se usa la misma estructura de datos para agregar nuevos objetos y recuperar los existentes. Por lo tanto, puede haber campos en cada estructura de datos que se omiten al agregar un nuevo objeto, ya que estos campos los rellena el motor de filtrado base (BFE) y no el autor de la llamada. Por ejemplo, una estructura de **datos \_ FWPM FILTER0** tiene un **campo filterId** que contiene **el LUID** del **FILTER0 de FWPS \_ correspondiente.** BFE asigna este **LUID** y, por tanto, este campo se omite en la llamada a [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de objetos](object-management.md)
</dt> </dl>

 

 





