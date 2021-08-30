---
title: Modelo de objetos
description: En la tabla siguiente se enumeran los tipos de objeto que se pueden manipular a través de los distintos conjuntos de API proporcionados por Windows Filtering Platform (WFP).
ms.assetid: 6931583f-785c-4e27-b5e4-d185d23a54ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f38d8530470affa5a62599b00de4c1cc2add604b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471091"
---
# <a name="object-model"></a>Modelo de objetos

En la tabla siguiente se enumeran los tipos de objeto que se pueden manipular a través de los distintos conjuntos de API proporcionados por Windows Filtering Platform (WFP).




| Tipo de objeto | Descripción | Propiedades de ejemplo | Ejemplo | 
|-------------|-------------|-------------------|---------|
| Filtrar | Regla que rige la clasificación. Si se cumplen las condiciones, se invoca la acción . <br /> Este es el objeto más complejo expuesto por WFP, ya que une todos los demás tipos de objeto. <br /> | <ul><li>Matriz de condiciones</li><li>Acción (Permitir, Bloquear, Llamar)</li><li><a href="filter-weight-assignment.md">Peso</a></li><li>Context</li></ul> | "Bloquear el tráfico con un puerto TCP mayor que 1024". <br /> "Llamada a IDS para todo el tráfico que no está protegido".<br /> | 
| Llamada | Conjunto de funciones que participan en el proceso de clasificación.<br /> Permite que el procesamiento de paquetes personalizados se haga cuando se cumplen ciertas condiciones.<br /> | <ul><li>ID</li><li>Capa aplicable</li></ul> | El controlador NAT<br /> | 
| Capa | Contenedor de filtros en el motor de filtros. <br /> Representa un punto específico en el procesamiento del tráfico de red donde se invoca el motor de filtro.<br /> | <ul><li>Esquema de los filtros que se pueden agregar a la capa</li></ul> | La capa de transporte de entrada<br /> | 
| Subcapa | Un sub componente de una capa, que se usa en el <a href="filter-arbitration.md">arbitraje de filtro.</a><br /> | <ul><li>Peso</li></ul> | Subcapa de Tunnel IPsec<br /> | 
| Proveedor | Proveedor de directivas que ha creado una solución en WFP.<br /> Se usa únicamente para la administración; no afecta al procesamiento de paquetes en tiempo de ejecución.<br /> | <ul><li>ID</li><li>Nombre del servicio</li></ul> | Firewall de Windows con seguridad avanzada<br /> Una aplicación de filtrado de direcciones URL de terceros<br /> | 
| Contexto del proveedor | Blob de datos utilizado por un proveedor de directivas para almacenar información de contexto arbitraria. <br /> Se usa para pasar información de configuración personalizada a una llamada.<br /> La manera más común de usar la información de contexto es hacer que los filtros hacen referencia a un contexto de proveedor. <br /> | <ul><li>ID</li><li>Blob en datos</li></ul> | IPsec almacena la configuración de autenticación en el motor de filtrado base (BFE). La propiedad "Context" de un filtro indica la configuración de autenticación que se usará para el tráfico que describe el filtro.<br /> La corrección de compatibilidad (shim) de selección de certificación SSL almacenará la información de certificación en un contexto de proveedor. <br /> | 




 

Los tipos de objeto expuestos por la API de WFP tienen una semántica coherente. Las acciones de agregar, enumerar, suscribir, y así sucesivamente son similares para todos los tipos de objeto.

Cada tipo de objeto se representa mediante una estructura de datos (por ejemplo, [**FWPM \_ FILTER0).**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0) Para minimizar el número de estructuras de datos diferentes expuestas por la API de WFP, se usa la misma estructura de datos para agregar nuevos objetos y recuperar los existentes. Por lo tanto, puede haber campos en cada estructura de datos que se omiten al agregar un nuevo objeto, ya que estos campos los rellena el motor de filtrado base (BFE) y no el autor de la llamada. Por ejemplo, una **estructura de datos \_ FWPM FILTER0** tiene un **campo filterId** que contiene el **LUID** del **FWPS \_ FILTER0 correspondiente.** BFE asigna este **LUID** y, por tanto, este campo se omite en la llamada a [**FwpmFilterAdd0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de objetos](object-management.md)
</dt> </dl>

 

 





