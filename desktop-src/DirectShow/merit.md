---
description: Los valores de mérito definen el orden en el que el administrador de gráficos de filtro intenta agregar filtros durante la creación del gráfico.
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: Mérito (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947a13d78f58c12c236ec31f0eeee1dc6d44f1d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678876"
---
# <a name="merit"></a>Fundament

Los valores de mérito definen el orden en el que el administrador de gráficos de filtro intenta agregar filtros durante la creación del gráfico.

<dl> <span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**Mérito \_ Mérito preferido** (0x800000) mérito <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **\_ normal** (0x600000) mérito <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> **\_ improbable** (0x400000) <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> **mérito \_ \_ no \_ use** (0x200000) el <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> **\_ \_ compresor** <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **\_ \_** de la mérito del software (0x100050).
</dl>

## <a name="remarks"></a>Observaciones

Cada filtro se registra con un valor de mérito. Cuando el administrador de gráficos de filtro genera un gráfico, enumera todos los filtros registrados con el tipo de medio correcto. A continuación, los prueba en orden de mérito, de mayor a menor. (Utiliza criterios adicionales para elegir entre los filtros con el mismo mérito). Nunca intenta los filtros con un valor de mérito menor o igual que el **mérito \_ no se \_ \_ usa**.

Un filtro que nunca debe tenerse en cuenta para la reproducción normal debe tener un mérito de **mérito \_ \_ no \_ usar** o menos. Los filtros se pueden registrar con valores intermedios no definidos por esta enumeración, como el **mérito \_ normal** + 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes y GUID](constants-and-guids.md)
</dt> <dt>

[Directrices para registrar filtros](guidelines-for-registering-filters.md)
</dt> <dt>

[Conexión inteligente](intelligent-connect.md)
</dt> </dl>

 

 




