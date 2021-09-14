---
description: La parte Etype/SAP del filtro de captura notifica al controlador Monitor de red que acepte fotogramas que tengan una combinación específica de Etypes y puntos de acceso de servicio (SAP).
ms.assetid: 57dcf1cd-f27f-4bd3-a5a8-9e978a2d213e
title: Escritura de la parte de filtro de Etype/SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b072d123ca18d3aa2b3f2c91db4a8461473a854
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161138"
---
# <a name="writing-etypesap-filter-portion"></a>Escritura de la parte de filtro de Etype/SAP

La parte Etype/SAP del filtro de captura notifica al controlador Monitor de red que acepte fotogramas que tengan una combinación específica de Etypes y puntos de acceso de servicio [](s.md) (SAP). Los tipos etypes y los SAP son formas en que los protocolos de bajo nivel, como Ethernet, LLC y Snap, indican qué protocolo los sigue. Concretamente:

-   Ethernet especifica un tipo Etype
-   LLC especifica un SAP
-   Snap especifica un tipo Etype

## <a name="etypesap-capture-filter-flags"></a>Marcas de filtro de captura de SAP/Etype

Use la siguiente información para establecer las marcas en el **miembro FilterFlags** de la [**estructura CAPTUREFILTER.**](capturefilter.md)



| Marca                                         | Significado                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LAS MARCAS \_ CAPTUREFILTER \_ INCLUYEN TODOS \_ LOS \_ SAPS   | Pasa todos los valores de SAP y notifica al controlador que todos los valores de SAP son válidos. Si se combina con cualquier valor del miembro **lpSapTable,** esta marca notifica al controlador que todos los valores de SAP excepto los de **lpSapTable** son válidos.<br/>           |
| LAS MARCAS \_ CAPTUREFILTER \_ INCLUYEN TODOS LOS \_ \_ ETYPES | Pasa todos los valores Etype y notifica al controlador que todos los valores Etype son válidos. Si se combina con cualquier valor del miembro **lpEtypeTable,** esta marca notifica al controlador que todos los valores Etype excepto los de **lpEtypeTable** son válidos.<br/> |
| CAPTUREFILTER \_ MARCA SOLO \_ \_ LOCALMENTE           | Al establecer esta marca, no se establecerá una NIC en modo P. Solo verá el tráfico local (los fotogramas que se van a usar en la máquina local).                                                                                                                                          |
| LAS MARCAS \_ CAPTUREFILTER \_ MANTIENEN SIN \_ PROCESAR             | Mantiene tramas MAC de anillo de token y SMT.                                                                                                                                                                                                                        |



 

## <a name="etypesap-capture-filter-settings"></a>Filtro de captura de Etype/SAP Configuración

Use la siguiente información para establecer los **miembros lpSapTable** y **lpEtypeTable** de la [**estructura CAPTUREFILTER.**](capturefilter.md)



| Parámetro          | Significado                                                                                                                                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **lpSapTable**   | Enumera los valores de SAP que desea que pase el controlador. Esta lista indica al controlador Monitor de red que valide cualquier fotograma que contenga una coincidencia. Si se establece CAPTUREFILTER FLAGS INCLUDE ALL SAPS, se convierte en una lista de excepciones (si se \_ \_ \_ \_ encuentra, no se pasa).           |
| **lpEtypeTable** | Enumera los valores Etype que desea que pase Monitor de red controlador. Esta lista solo indica al controlador que valide cualquier fotograma que contenga una coincidencia. Si se establece CAPTUREFILTER \_ FLAGS INCLUDE ALL ETYPES, se convierte en una lista de excepciones (si se \_ \_ \_ encuentra, no se pasa). |



 

 

 




