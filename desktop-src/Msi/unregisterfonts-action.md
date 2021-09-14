---
description: La acción UnregisterFonts quita la información de registro sobre las fuentes instaladas del sistema.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Acción UnregisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc847203b72b0e2d92fb5e9a4dc465bebb001b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171577"
---
# <a name="unregisterfonts-action"></a>Acción UnregisterFonts

La acción UnregisterFonts quita la información de registro sobre las fuentes instaladas del sistema.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Se debe llamar a la acción [RemoveFiles](removefiles-action.md) después de UnregisterFonts.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Archivo de fuente.                 |



 

## <a name="remarks"></a>Observaciones

La acción UnregisterFonts se ejecuta si el archivo especificado en la columna Archivo de la tabla Fuente pertenece a un \_ componente que se está desinstalando. [](font-table.md)

 

 



