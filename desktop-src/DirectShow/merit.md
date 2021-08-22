---
description: Los valores de la propiedad definen el orden en el que el administrador Graph filtro intenta agregar filtros durante la creación del grafo.
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: Fundamento (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a55c112f1a08d63e45d5385f525371ae9642c1b01a1b4af5d7747b042efffe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073019"
---
# <a name="merit"></a>Mérito

Los valores de la propiedad definen el orden en el que el administrador Graph filtro intenta agregar filtros durante la creación del grafo.

<dl> <span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**LUGAR DE LA CONS \_ PREFERITORIO** (0x800000) LA NORMAL DE CONSERCIÓN NORMAL (0x600000) IMPROBABLE (0x400000) NO USE <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **\_** <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> **\_** <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> (0x200000) EL 0X100000) **\_ \_ \_** <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> **\_ \_** <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **\_ \_** DE LA CONSORTE (0x100050)
</dl>

## <a name="remarks"></a>Comentarios

Cada filtro se registra con un valor de merececión. Cuando el administrador de gráficos de filtro compila un gráfico, enumera todos los filtros registrados con el tipo de medio correcto. A continuación, los prueba en orden de consenso, de mayor a menor. (Usa criterios adicionales para elegir entre filtros con el mismo criterio). Nunca intenta filtros con un valor de merececión menor o igual que **NO \_ \_ \_ USE .**

Un filtro que nunca se debe tener en cuenta para la reproducción normal debe tener el valor **DE NO USAR NI \_ \_ \_ USAR** NI mucho menos. Los filtros se pueden registrar con valores intermedios no definidos por esta enumeración, como **LA NORMAL + \_** 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes y GUID](constants-and-guids.md)
</dt> <dt>

[Directrices para registrar filtros](guidelines-for-registering-filters.md)
</dt> <dt>

[Inteligencia Conectar](intelligent-connect.md)
</dt> </dl>

 

 




