---
description: Especifica si una transformación de Media Foundation (MFT) solo se registra en el proceso de aplicaciones.
ms.assetid: e10d6378-8e85-4f73-9fa3-a2e954fc8249
title: MFT_PROCESS_LOCAL_Attribute atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d3595ef530008b8d09f27e3e76fad81a06039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811606"
---
# <a name="mft_process_local_attribute-attribute"></a>\_Atributo de \_ atributo local de proceso de MFT \_

Especifica si una transformación de Media Foundation (MFT) solo se registra en el proceso de la aplicación.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Este atributo se usa como se indica a continuación:

1.  La aplicación registra un MFT local llamando a la función [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) o [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) . Estas funciones registran la MFT en el proceso de la aplicación.
2.  Se llama a la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para enumerar MFTs que coinciden con un determinado conjunto de criterios. La aplicación podría llamar directamente a la función **MFTEnumEx** , pero el cargador de topología llama a esta función con mayor frecuencia.
3.  La función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) recupera una matriz de punteros de [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , cada uno de los cuales representa un objeto de activación para una MFT. Si una MFT se registra localmente, el \_ atributo de \_ atributo local del proceso MFT \_ se establece en **true** en el objeto de activación correspondiente.

El valor predeterminado de este atributo es **false**.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de transformación](transform-attributes.md)
</dt> </dl>

 

 




