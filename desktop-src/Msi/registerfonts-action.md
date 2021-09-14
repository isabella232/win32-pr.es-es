---
description: La acción RegisterFonts registra las fuentes instaladas con el sistema. Esta acción asigna el nombre de fuente de la columna FontTitle de la tabla Font a la ruta de acceso del archivo de fuente instalado.
ms.assetid: 3c6d3ec9-b36f-46f4-8b32-c97a75b9e238
title: Acción RegisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98532be2744e89fff79f6e3d8becd2e6cc9259a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069695"
---
# <a name="registerfonts-action"></a>Acción RegisterFonts

La acción RegisterFonts registra las fuentes instaladas con el sistema. Esta acción asigna el nombre de fuente de la columna FontTitle de la [tabla Font](font-table.md) a la ruta de acceso del archivo de fuente instalado.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Se [debe llamar a la acción InstallFiles](installfiles-action.md) antes de llamar a la acción RegisterFonts.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Archivo de fuente.                 |



 

## <a name="remarks"></a>Observaciones

La acción RegisterFonts se ejecuta si el archivo especificado en la columna Archivo de la tabla Font pertenece \_ a un componente que se está instalando. [](font-table.md)

 

 



