---
description: La acción UnregisterFonts quita del sistema la información de registro sobre las fuentes instaladas.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Acción UnregisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc847203b72b0e2d92fb5e9a4dc465bebb001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678524"
---
# <a name="unregisterfonts-action"></a>Acción UnregisterFonts

La acción UnregisterFonts quita del sistema la información de registro sobre las fuentes instaladas.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Se debe llamar a la acción [RemoveFiles](removefiles-action.md) después de UnregisterFonts.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Archivo de fuente.                 |



 

## <a name="remarks"></a>Observaciones

La acción UnregisterFonts se ejecuta si el archivo especificado en la \_ columna de archivo de la [tabla de fuentes](font-table.md) pertenece a un componente que se va a desinstalar.

 

 



