---
title: VBRPeak
description: El atributo VBRPeak contiene la velocidad de bits más alta en una secuencia codificada de velocidad de bits variable (VBR).
ms.assetid: 7b735145-8235-4efb-986f-952989b739bc
keywords:
- VBRPeak formato de Windows Media
topic_type:
- apiref
api_name:
- VBRPeak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8aacb076c3e92cfa676e73e945506cc4942bf4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076840"
---
# <a name="vbrpeak"></a>VBRPeak

El atributo **VBRPeak** contiene la velocidad de bits más alta en una secuencia codificada de velocidad de bits variable (VBR).

## <a name="global-constant"></a>Constante global

g \_ wszVBRPeak

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ DWORD**

## <a name="remarks"></a>Observaciones

Al tener acceso a la interfaz **IWMHeaderInfo3** del objeto escritor, puede Agregar o cambiar este valor. En otros objetos (editor de metadatos, lector y lector sincrónico), este valor es de solo lectura.

El escritor escribe automáticamente un valor de **VBRPeak** para cada secuencia VBR.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




