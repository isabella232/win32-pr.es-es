---
title: VBRPeak
description: El atributo VBRPeak contiene la mayor velocidad de bits momentánaria en una secuencia codificada con velocidad de bits variable (VBR).
ms.assetid: 7b735145-8235-4efb-986f-952989b739bc
keywords:
- Formato multimedia de Windows VBRPeak
topic_type:
- apiref
api_name:
- VBRPeak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9163e64aa3d309af8fd35626b7a4c0397ba4c949213ef351c1ac73ee9575a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704845"
---
# <a name="vbrpeak"></a>VBRPeak

El **atributo VBRPeak** contiene la mayor velocidad de bits momentánaria en una secuencia codificada con velocidad de bits variable (VBR).

## <a name="global-constant"></a>Constante global

g \_ wszVBRPeak

## <a name="data-type"></a>Tipo de datos

**DWORD \_ DE TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Al acceder a **la interfaz IWMHeaderInfo3** del objeto de escritor, puede agregar o cambiar este valor. En otros objetos (editor de metadatos, lector y lector sincrónico), este valor es de solo lectura.

El sistema de escritura escribe automáticamente un **valor VBRPeak** para cada secuencia de VBR.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




