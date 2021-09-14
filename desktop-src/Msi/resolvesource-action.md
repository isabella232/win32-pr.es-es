---
description: La acción ResolveSource determina la ubicación del origen y establece la propiedad SourceDir si el origen aún no se ha resuelto.
ms.assetid: 6d6205a0-a870-4df2-922b-befea7e28a1a
title: Acción ResolveSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713598cd4daa90764cde2155e43b61e151432d31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069653"
---
# <a name="resolvesource-action"></a>Acción ResolveSource

La acción ResolveSource determina la ubicación del origen y establece la [**propiedad SourceDir**](sourcedir.md) si el origen aún no se ha resuelto.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción ResolveSource debe ir después de [la acción CostInitialize](costinitialize-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Observaciones

Se debe llamar a la acción ResolveSource antes de usar [**la propiedad SourceDir**](sourcedir.md) en cualquier expresión. También debe llamarse antes de intentar recuperar el valor de la **propiedad SourceDir** mediante [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya). La acción ResolveSource no debe ejecutarse cuando el origen no está disponible, como puede ser al desinstalar la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 



