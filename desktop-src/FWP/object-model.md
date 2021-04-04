---
title: Modelo de objetos
description: En la tabla siguiente se enumeran los tipos de objeto que se pueden manipular a través de los distintos conjuntos de API proporcionados por la plataforma de filtrado de Windows (WFP).
ms.assetid: 6931583f-785c-4e27-b5e4-d185d23a54ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa90b4757a39617616c6f83b6b79fe322b2e64c8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104077360"
---
# <a name="object-model"></a>Modelo de objetos

En la tabla siguiente se enumeran los tipos de objeto que se pueden manipular a través de los distintos conjuntos de API proporcionados por la plataforma de filtrado de Windows (WFP).



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
<td>Filter</td>
<td>Una regla que rige la clasificación. Si se cumplen las condiciones, se invoca la acción. <br/> Este es el objeto más complejo expuesto por WFP, ya que une todos los demás tipos de objeto. <br/></td>
<td><ul>
<li>Matriz de condiciones</li>
<li>Acción (permitir, bloquear, llamada)</li>
<li><a href="filter-weight-assignment.md">Peso</a></li>
<li>Context</li>
</ul></td>
<td>&quot;Bloquee el tráfico con un puerto TCP superior a 1024.&quot; <br/> &quot;Llamada a los IDENTIFICADOres para todo el tráfico que no está protegido.&quot;<br/></td>
</tr>
<tr class="even">
<td>Llamada</td>
<td>Conjunto de funciones que participan en el proceso de clasificación.<br/> Permite que se realice el procesamiento personalizado de paquetes cuando se cumplen determinadas condiciones.<br/></td>
<td><ul>
<li>id</li>
<li>Nivel aplicable</li>
</ul></td>
<td>El controlador NAT<br/></td>
</tr>
<tr class="odd">
<td>Nivel</td>
<td>Un contenedor de filtros en el motor de filtro. <br/> Representa un punto específico en el procesamiento del tráfico de red donde se invoca el motor de filtro.<br/></td>
<td><ul>
<li>Esquema para los filtros que se pueden agregar a la capa</li>
</ul></td>
<td>La capa de transporte de entrada<br/></td>
</tr>
<tr class="even">
<td>Capa secundaria</td>
<td>Un subcomponente de una capa, que se usa en el <a href="filter-arbitration.md">arbitraje de filtros</a>.<br/></td>
<td><ul>
<li>Peso</li>
</ul></td>
<td>La subcapa del túnel IPsec<br/></td>
</tr>
<tr class="odd">
<td>Proveedor</td>
<td>Un proveedor de directivas que ha compilado una solución en WFP.<br/> Se utiliza únicamente para la administración; no afecta al procesamiento de paquetes en tiempo de ejecución.<br/></td>
<td><ul>
<li>id</li>
<li>Nombre del servicio</li>
</ul></td>
<td>Firewall de Windows con seguridad avanzada<br/> Una aplicación de filtrado de direcciones URL de terceros<br/></td>
</tr>
<tr class="even">
<td>Contexto de proveedor</td>
<td>Un BLOB de datos utilizado por un proveedor de directivas para almacenar información de contexto arbitrario. <br/> Se usa para pasar información de configuración personalizada a una llamada.<br/> La forma más común de usar la información de contexto es que los filtros hagan referencia a un contexto de proveedor. <br/></td>
<td><ul>
<li>id</li>
<li>BLOB de datos</li>
</ul></td>
<td>IPsec almacena la configuración de autenticación en el motor de filtrado de base (BFE). La &quot; &quot; propiedad de contexto de un filtro indica la configuración de autenticación que se va a usar para el tráfico que describe el filtro.<br/> La corrección de compatibilidad de la selección de certificación SSL almacenará la información de certificación en un contexto de proveedor. <br/></td>
</tr>
</tbody>
</table>



 

Los tipos de objeto expuestos por la API de WFP tienen una semántica coherente. Las acciones de agregar, enumerar, suscribir, etc., son similares para todos los tipos de objeto.

Cada tipo de objeto se representa mediante una estructura de datos (por ejemplo, [**FWPM \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)). Con el fin de minimizar el número de estructuras de datos diferentes que expone la API de WFP, se usa la misma estructura de datos para agregar nuevos objetos y recuperar los existentes. Por lo tanto, puede haber campos en cada estructura de datos que se omitan al agregar un nuevo objeto, ya que estos campos los rellenará el motor de filtrado de base (BFE), y no el llamador. Por ejemplo, una estructura de datos de **FWPM \_ FILTER0** tiene un campo **FilterId** que contiene el **LUID** del **FWPS \_ FILTER0** correspondiente. BFE asigna este **LUID** y, por lo tanto, este campo se omite en la llamada a [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de objetos](object-management.md)
</dt> </dl>

 

 





