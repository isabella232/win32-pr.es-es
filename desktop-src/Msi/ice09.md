---
description: ICE09 valida que el bit permanente está establecido para cada componente marcado para la instalación en SystemFolder.
ms.assetid: b4e11d75-4214-49de-ac12-6f360771ad73
title: ICE09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c890189e69fc7473e96909af368e5905877dca9d43f32ebcc2903fcf25fc6a5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129445"
---
# <a name="ice09"></a>ICE09

ICE09 valida que el bit permanente está establecido para cada componente marcado para la instalación en SystemFolder. ICE09 envía una advertencia porque debe evitar la instalación de componentes del sistema no permanentes en SystemFolder. Para evitar esta advertencia, establezca el bit Permanente en la columna Atributos de la tabla [Component](component-table.md) para todos los componentes marcados para la instalación en SystemFolder. No se realiza ninguna validación si la base de datos no tiene una tabla Component.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



