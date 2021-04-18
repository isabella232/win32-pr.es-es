---
description: Establece el número máximo de iteraciones de búsqueda que usará el origen de medios ASF cuando realice búsquedas iterativas.
ms.assetid: 5b596faf-1217-424d-ae16-8c9ec6f31af1
title: Propiedad MFPKEY_ASFMediaSource_IterativeSeek_Max_Count (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfb9268f1def2ab0d489f58cafa0b1720196c7ac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697970"
---
# <a name="mfpkey_asfmediasource_iterativeseek_max_count-property"></a>MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ \_ propiedad Count Max

Establece el número máximo de iteraciones de búsqueda que usará el origen de medios ASF cuando realice búsquedas iterativas.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Observaciones

Utilice esta propiedad para configurar el origen de medios ASF. Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

Esta propiedad solo se aplica cuando está habilitada la búsqueda iterativa. Para obtener más información, consulte [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

El intervalo válido de esta propiedad es \[ 1-10 \] , ambos inclusive. Con un número mayor, la búsqueda iterativa tiende a ser más precisa, pero tarda más tiempo.

El valor predeterminado es 5.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




