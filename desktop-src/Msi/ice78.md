---
description: ICE78 comprueba que la tabla AdvtUISequence no existe o está vacía. Esto es necesario porque no se permite ninguna interfaz de usuario durante la publicidad.
ms.assetid: 8ed1c68f-331d-42f9-80df-bdcb42962482
title: ICE78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8993a0a03b0f70bf2d99511782bc9b7d259d4c9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074539"
---
# <a name="ice78"></a>ICE78

ICE78 comprueba que la [tabla AdvtUISequence](advtuisequence-table.md) no existe o está vacía. Esto es necesario porque no se permite ninguna interfaz de usuario durante la publicidad.

## <a name="result"></a>Resultado

ICE78 publica un error si la tabla AdvtUISequence existe y no está vacía.

## <a name="example"></a>Ejemplo

ICE78 notifica el siguiente error para el ejemplo:

La acción "Action1" se encuentra en la tabla AdvtUISequence. No se permite ninguna interfaz de usuario durante la publicidad. Por lo tanto, la tabla AdvtUISequence debe estar vacía o no estar presente.

[Tabla AdvtUISequence](advtuisequence-table.md)(parcial)



| Acción  | Condición | Secuencia |
|---------|-----------|----------|
| Action1 | true      | 1        |



 

Para corregir el error, quite "Action1" de la tabla o quite la tabla.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



