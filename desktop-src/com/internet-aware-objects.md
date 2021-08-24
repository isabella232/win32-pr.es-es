---
title: Internet-Aware objetos
description: Internet-Aware objetos
ms.assetid: a8228431-5a07-4816-938d-c789ab6a8eaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280141d4bc9cb1a6a6c685c4badde0b24609996683e73c74f69637440b39ef8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756155"
---
# <a name="internet-aware-objects"></a>Internet-Aware objetos

Hay determinadas categorías identificadas para cubrir las interfaces de persistencia; se han identificado como resultado de definir cómo funcionan los controles a través de Internet. Un contenedor que no admite toda la gama de interfaces de persistencia debe asegurarse de que no hospeda un control que requiera una combinación de interfaces que no admite.

En las tablas siguientes se describe el significado de varias categorías como categorías implementadas y obligatorias.



| Categorías requeridas                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CATID \_ PersistsToMoniker, CATID \_ PersistsToStreamInit, CATID \_ PersisitsToStream, CATID \_ PersistsToStorage, CATID \_ PersistsToMemory, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag<br/> | Cada una de estas categorías es mutuamente excluyente y solo se usa cuando un objeto solo admite un mecanismo de persistencia (de ahí la exclusión mutua). Los contenedores que no admiten el mecanismo de persistencia descrito por una de estas categorías deben impedir que creen objetos de clases tan marcados.<br/> |
| CATID \_ RequiresDataPathHost<br/>                                                                                                                                                             | El objeto requiere la capacidad de guardar datos en una o varias rutas de acceso y requiere la participación del contenedor, por lo que requiere compatibilidad con contenedores [**para IBindHost.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85))<br/>                                                                                                                                  |



 



| Categorías implementadas                                                                                                                                                                            | Descripción                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| CATID \_ PersistsToMoniker, CATID \_ PersistsToStreamInit, CATID \_ PersistsToStream, CATID \_ PersistsToStorage, CATID \_ PersistsToMemory, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag<br/> | El objeto admite el mecanismo IPersist \* correspondiente para la categoría.<br/> |



 

En la tabla siguiente se proporcionan los CATID exactos asignados a cada categoría:



| Category                                | CATID                                           |
|-----------------------------------------|-------------------------------------------------|
| CATID \_ RequiresDataPathHost<br/>  | 0de86a50-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToMoniker <br/>    | 0de86a51-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToStorage <br/>    | 0de86a52-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToStreamInit <br/> | 0de86a53-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToStream <br/>     | 0de86a54-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToMemory <br/>     | 0de86a55-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToFile <br/>       | 0de86a56-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToPropertyBag<br/> | 0de86a57-2baa-11cf-a229-00aa003d7352<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías del componente](component-categories.md)
</dt> </dl>

 

