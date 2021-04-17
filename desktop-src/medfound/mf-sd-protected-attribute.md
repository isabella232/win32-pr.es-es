---
description: Indica si una secuencia contiene contenido protegido.
ms.assetid: 1c1a201c-4b55-4b86-a08f-d06c1a7db29d
title: MF_SD_PROTECTED atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c97320d15353b8e23a43fa4efac2e5883a7366f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717003"
---
# <a name="mf_sd_protected-attribute"></a>\_ \_ Atributo protegido de MF SD

Indica si una secuencia contiene contenido protegido.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Trata como un valor booleano.

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de flujo. Si el valor del atributo es **true**, el flujo contiene contenido protegido. Si el valor es **false** o no se establece el atributo, el flujo contiene un contenido sin cifrar.

En lugar de comprobar cada secuencia para este atributo, puede pasar un descriptor de presentación a la función [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) . Esta función comprueba si el descriptor de presentación contiene cualquier flujo protegido.

Un origen multimedia debe establecer este atributo en el descriptor de flujo si el contenido requiere la ruta de acceso a medios protegidos (PMP).

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="examples"></a>Ejemplos


```
// This function returns TRUE if the stream contains protected 
// content. You can also call the MFRequireProtectedEnvironment 
// function to test whether a presentation contains any streams
// with protected content.

BOOL StreamHasProtectedContent(IMFStreamDescriptor *pSD)
{
    return MFGetAttributeUINT32(pSD, MF_SD_PROTECTED, FALSE);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Atributos de descriptor de secuencia](stream-descriptor-attributes.md)
</dt> </dl>

 

 




