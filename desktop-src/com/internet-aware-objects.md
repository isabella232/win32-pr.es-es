---
title: Objetos Internet-Aware
description: Objetos Internet-Aware
ms.assetid: a8228431-5a07-4816-938d-c789ab6a8eaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 806b8887309760417247cb176c84cda1605bd5aa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995675"
---
# <a name="internet-aware-objects"></a>Objetos Internet-Aware

Existen ciertas categorías identificadas para cubrir las interfaces de persistencia; se han identificado como resultado de la definición del modo en que los controles funcionan a través de Internet. Un contenedor que no admite el intervalo completo de interfaces persistencia debe asegurarse de que no hospeda un control que requiera una combinación de interfaces que no admita.

En las tablas siguientes se describe el significado de varias categorías como categorías implementadas y necesarias.



| Categorías requeridas                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CATId \_ PersistsToMoniker, CATID \_ PERSISTSTOSTREAMINIT, CATID \_ PersisitsToStream, CATID \_ PersistsToStorage, CATId \_ PersistsToMemory, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag<br/> | Cada una de estas categorías es mutuamente excluyente y solo se usa cuando un objeto solo admite un mecanismo de persistencia en absoluto (por lo tanto, la exclusión mutua). Los contenedores que no admiten el mecanismo de persistencia descrito por una de estas categorías deben evitar que se creen objetos de clases, por lo que se marcan como.<br/> |
| CATId \_ RequiresDataPathHost<br/>                                                                                                                                                             | El objeto requiere la capacidad de guardar los datos en una o varias rutas de acceso y requiere la implicación del contenedor, por lo que se necesita compatibilidad con contenedores para [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).<br/>                                                                                                                                  |



 



| Categorías implementadas                                                                                                                                                                            | Descripción                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| CATId \_ PersistsToMoniker, CATID \_ PERSISTSTOSTREAMINIT, CATID \_ PersistsToStream, CATID \_ PersistsToStorage, CATId \_ PersistsToMemory, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag<br/> | El objeto admite el mecanismo IPersist correspondiente \* para la categoría.<br/> |



 

En la tabla siguiente se proporcionan los CATID exactos asignados a cada categoría:



| Category                                | CATID                                           |
|-----------------------------------------|-------------------------------------------------|
| CATId \_ RequiresDataPathHost<br/>  | 0de86a50-2baa-11cf-a229-00aa003d7352<br/> |
| CATId \_ PersistsToMoniker <br/>    | 0de86a51-2baa-11cf-a229-00aa003d7352<br/> |
| CATId \_ PersistsToStorage <br/>    | 0de86a52-2baa-11cf-a229-00aa003d7352<br/> |
| CATId \_ PersistsToStreamInit <br/> | 0de86a53-2baa-11cf-a229-00aa003d7352<br/> |
| CATId \_ PersistsToStream <br/>     | 0de86a54-2baa-11cf-a229-00aa003d7352<br/> |
| CATId \_ PersistsToMemory <br/>     | 0de86a55-2baa-11cf-a229-00aa003d7352<br/> |
| CATId \_ PersistsToFile <br/>       | 0de86a56-2baa-11cf-a229-00aa003d7352<br/> |
| CATId \_ PersistsToPropertyBag<br/> | 0de86a57-2baa-11cf-a229-00aa003d7352<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías del componente](component-categories.md)
</dt> </dl>

 

