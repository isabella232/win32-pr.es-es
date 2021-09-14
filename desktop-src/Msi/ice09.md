---
description: ICE09 valida que el bit permanente se establece para cada componente marcado para la instalación en SystemFolder.
ms.assetid: b4e11d75-4214-49de-ac12-6f360771ad73
title: ICE09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01cd20a1b354888877be0f5d456b6d6af2bdec82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074672"
---
# <a name="ice09"></a>ICE09

ICE09 valida que el bit permanente se establece para cada componente marcado para la instalación en SystemFolder. ICE09 envía una advertencia porque debe evitar la instalación de componentes del sistema no permanentes en SystemFolder. Para evitar esta advertencia, establezca el bit Permanente en la columna Atributos de la tabla [Componente](component-table.md) para todos los componentes marcados para la instalación en SystemFolder. No se realiza ninguna validación si la base de datos no tiene una tabla Component.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



