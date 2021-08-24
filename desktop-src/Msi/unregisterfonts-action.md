---
description: La acción UnregisterFonts quita la información de registro sobre las fuentes instaladas del sistema.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Acción UnregisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ec15a7a431a03d678fb2fd8c39460ea40ebbcadf3efd0c24814c84e6042fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787005"
---
# <a name="unregisterfonts-action"></a>Acción UnregisterFonts

La acción UnregisterFonts quita la información de registro sobre las fuentes instaladas del sistema.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Se debe llamar a la acción [RemoveFiles](removefiles-action.md) después de UnregisterFonts.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Archivo de fuente.                 |



 

## <a name="remarks"></a>Comentarios

La acción UnregisterFonts se ejecuta si el archivo especificado en la columna Archivo de la tabla Font pertenece \_ a un componente que se está desinstalando. [](font-table.md)

 

 



