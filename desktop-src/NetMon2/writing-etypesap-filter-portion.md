---
description: La parte Etype/SAP del filtro de captura notifica al controlador Monitor de red que acepte fotogramas que tengan una combinación específica de Etypes y puntos de acceso de servicio (SAP).
ms.assetid: 57dcf1cd-f27f-4bd3-a5a8-9e978a2d213e
title: Escritura de la parte del filtro Etype/SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da18b8e2d7d5fc081ea941070644379e6e988a5c697b7ee09ee76a8fdd0c083e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036795"
---
# <a name="writing-etypesap-filter-portion"></a>Escritura de la parte del filtro Etype/SAP

La parte Etype/SAP del filtro de captura notifica al controlador Monitor de red que acepte fotogramas [](s.md) que tengan una combinación específica de Etypes y puntos de acceso de servicio (SAP). Los tipos Etypes y SAP son dos maneras en que los protocolos de bajo nivel, como Ethernet, LLC y Snap, indican qué protocolo los sigue. En concreto:

-   Ethernet especifica un tipo Etype
-   LLC especifica un SAP
-   Snap especifica un tipo Etype

## <a name="etypesap-capture-filter-flags"></a>Marcas de filtro Etype/SAP Capture

Use la siguiente información para establecer las marcas en el **miembro FilterFlags** de la [**estructura CAPTUREFILTER.**](capturefilter.md)



| Marca                                         | Significado                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LAS MARCAS \_ DE CAPTUREFILTER \_ INCLUYEN TODOS \_ LOS \_ SAP   | Pasa todos los valores de SAP y notifica al controlador que todos los valores de SAP son válidos. Si se combina con cualquier valor del miembro **lpSapTable,** esta marca notifica al controlador que todos los valores de SAP excepto los de **lpSapTable** son válidos.<br/>           |
| LAS MARCAS \_ DE CAPTUREFILTER \_ INCLUYEN TODOS \_ LOS \_ ETYPES | Pasa todos los valores Etype y notifica al controlador que todos los valores Etype son válidos. Si se combina con cualquier valor del miembro **lpEtypeTable,** esta marca notifica al controlador que todos los valores Etype excepto los de **lpEtypeTable** son válidos.<br/> |
| CAPTUREFILTER \_ SOLO MARCA LAS MARCAS \_ \_ LOCALES           | Al establecer esta marca, no se establecerá una NIC en modo P. Solo verá el tráfico local (cualquier fotograma a la máquina local).                                                                                                                                          |
| LAS MARCAS DE CAPTUREFILTER \_ \_ SE MANTIENEN SIN \_ PROCESAR             | Mantiene tramas MAC de anillo de token y SMT.                                                                                                                                                                                                                        |



 

## <a name="etypesap-capture-filter-settings"></a>Filtro de captura de Etype/SAP Configuración

Use la siguiente información para establecer los **miembros lpSapTable** y **lpEtypeTable** de la [**estructura CAPTUREFILTER.**](capturefilter.md)



| Configuración          | Significado                                                                                                                                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **lpSapTable**   | Enumera los valores de SAP que desea que pase el controlador. Esta lista indica al controlador Monitor de red que valide cualquier fotograma que contenga una coincidencia. Si se establece CAPTUREFILTER FLAGS INCLUDE ALL SAPS, se convierte en una lista de \_ \_ \_ excepciones (si se \_ encuentra, no se pasa).           |
| **lpEtypeTable** | Enumera los valores Etype que desea que pase Monitor de red controlador. Solo esta lista indica al controlador que valide cualquier fotograma que contenga una coincidencia. Si se establece CAPTUREFILTER \_ FLAGS INCLUDE ALL ETYPES, se convierte en una lista de excepciones (si se \_ \_ \_ encuentra, no se pasa). |



 

 

 




