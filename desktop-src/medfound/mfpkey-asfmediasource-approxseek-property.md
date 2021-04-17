---
description: Especifica si el origen de medios ASF utiliza búsquedas aproximadas.
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: Propiedad MFPKEY_ASFMediaSource_ApproxSeek (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253a18ebbdf78e3aa0ef0e79f41c4bf180a04b48
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697972"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a>\_ \_ Propiedad APPROXSEEK de MFPKEY ASFMediaSource

Especifica si el origen de medios ASF utiliza búsquedas aproximadas.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**VARIANTE \_ bool**

VT \_ bool

**boolVal**



## <a name="remarks"></a>Observaciones

Las aplicaciones pueden utilizar esta propiedad para configurar el origen de medios ASF. Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

El origen de medios ASF controla la búsqueda de la manera siguiente:

-   Si el valor de esta propiedad es **Variant \_ true**, el origen multimedia utiliza una búsqueda aproximada, que es menos precisa pero más rápida que la búsqueda exacta.
-   Si el valor es **Variant \_ false** y el archivo ASF tiene un índice, el origen multimedia utiliza una búsqueda exacta.
-   Si el archivo ASF no contiene un índice, el origen del medio usa la búsqueda de approxmate a menos que la propiedad [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) esté establecida en **Variant \_ true**.
-   Si el archivo ASF no contiene un índice y la propiedad [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) es **Variant \_ true**, el origen multimedia utiliza búsquedas iterativas. La búsqueda iterativa es más precisa pero más lenta que la búsqueda aproximada (pero generalmente menos precisa que la búsqueda exacta).
    > [!Note]  
    > Requiere Windows 7.

     

El valor predeterminado de esta propiedad es **Variant \_ false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




