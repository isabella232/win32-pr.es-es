---
description: La parte de ETYPE/SAP del filtro de captura notifica al controlador de Monitor de red para que acepte fotogramas que tengan una combinación específica de ETYPE y puntos de acceso de servicio (SAP).
ms.assetid: 57dcf1cd-f27f-4bd3-a5a8-9e978a2d213e
title: Escribir la parte de filtro de ETYPE/SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b072d123ca18d3aa2b3f2c91db4a8461473a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002555"
---
# <a name="writing-etypesap-filter-portion"></a>Escribir la parte de filtro de ETYPE/SAP

La parte de ETYPE/SAP del filtro de captura notifica al controlador de Monitor de red para que acepte fotogramas que tengan una combinación específica de ETYPE y [*puntos de acceso de servicio*](s.md) (SAP). ETYPE y SAP son formas en que los protocolos de bajo nivel, como Ethernet, LLC y Snap, indican qué protocolo los sigue. De manera específica:

-   Ethernet especifica un ETYPE
-   LLC especifica un SAP
-   Ajustar especifica un ETYPE

## <a name="etypesap-capture-filter-flags"></a>ETYPE/marcas de filtro de captura de SAP

Utilice la siguiente información para establecer las marcas en el miembro **FilterFlags** de la estructura [**CAPTUREFILTER**](capturefilter.md) .



| Marca                                         | Significado                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_las marcas de CAPTUREFILTER \_ incluyen \_ todos los \_ SAP   | Pasa todos los valores de SAP y notifica al controlador que todos los valores de SAP son válidos. Si se combina con cualquier valor del miembro **lpSapTable** , esta marca notifica al controlador que todos los valores de SAP excepto los de **lpSapTable** son válidos.<br/>           |
| \_las marcas de CAPTUREFILTER \_ incluyen \_ todos los \_ ETYPE | Pasa todos los valores ETYPE y notifica al controlador que todos los valores ETYPE son válidos. Si se combina con cualquier valor del miembro **lpEtypeTable** , esta marca notifica al controlador que todos los valores ETYPE excepto los de **lpEtypeTable** son válidos.<br/> |
| \_marcas de \_ CAPTUREFILTER \_ solo locales           | Al establecer esta marca, no se establecerá una NIC en modo P. Solo verá el tráfico local (cualquier fotograma al equipo local).                                                                                                                                          |
| las \_ marcas CAPTUREFILTER \_ siguen \_ sin procesar             | Mantiene fotogramas MAC de SMT y token ring.                                                                                                                                                                                                                        |



 

## <a name="etypesap-capture-filter-settings"></a>ETYPE/configuración del filtro de captura de SAP

Use la siguiente información para establecer los miembros **lpSapTable** y **lpEtypeTable** de la estructura [**CAPTUREFILTER**](capturefilter.md) .



| Configuración          | Significado                                                                                                                                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **lpSapTable**   | Muestra los valores de SAP que desea que el controlador pase. Esta lista indica al controlador de Monitor de red para validar cualquier marco que contenga una coincidencia. Si \_ las marcas \_ de CAPTUREFILTER incluyen \_ \_ la configuración de todos los SAP, se convierte en una lista de excepciones (si se encuentra, no pasa).           |
| **lpEtypeTable** | Muestra los valores ETYPE que desea que pase el controlador Monitor de red. Esta lista solo indica al controlador que valide cualquier marco que contenga una coincidencia. Si \_ las marcas \_ de CAPTUREFILTER incluyen \_ \_ la configuración de ETYPE, se convierte en una lista de excepciones (si se encuentra, no pasa). |



 

 

 




