---
description: Los valores de medición definen el orden en el que el Administrador de Graph intenta agregar filtros durante la creación del grafo.
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: Fundamento (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947a13d78f58c12c236ec31f0eeee1dc6d44f1d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072162"
---
# <a name="merit"></a>Mérito

Los valores de medición definen el orden en el que el Administrador de Graph intenta agregar filtros durante la creación del grafo.

<dl> <span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**LUGAR \_ PREFERITORIO** (0x800000) LA NORMAL DE NORMALIDAD (0x600000) NO ES PROBABLE (0x400000) NO USE (0x200000) INSERTE (0x100000) INSERTE <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **\_** <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> **\_** <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> **\_ \_ \_** <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> **\_ \_** <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **\_ \_** (0x100050)
</dl>

## <a name="remarks"></a>Observaciones

Cada filtro se registra con un valor de meritorio. Cuando el administrador de gráficos de filtros compila un gráfico, enumera todos los filtros registrados con el tipo de medio correcto. A continuación, los prueba en orden de mes, de mayor a menor. (Usa criterios adicionales para elegir entre filtros con el mismo criterio). Nunca intenta los filtros con un valor de meritorio menor o igual que **NO \_ USE \_ \_ .**

Un filtro que nunca se debe tener en cuenta para la reproducción normal debe tener un fundamento de **NO USAR NI \_ \_ \_ USAR** NI mucho menos. Los filtros se pueden registrar con valores intermedios no definidos por esta enumeración, como **SE NORMAL + \_** 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes y GUID](constants-and-guids.md)
</dt> <dt>

[Directrices para registrar filtros](guidelines-for-registering-filters.md)
</dt> <dt>

[Inteligencia Conectar](intelligent-connect.md)
</dt> </dl>

 

 




