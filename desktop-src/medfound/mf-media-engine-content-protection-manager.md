---
description: Permite que el motor multimedia reprodgue contenido protegido.
ms.assetid: F6F17EC7-6553-4127-B691-C20C945DD4D8
title: MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER atributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb99d1df36c9b9adbf1c099d619df60e1144b87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360459"
---
# <a name="mf_media_engine_content_protection_manager-attribute"></a>Atributo CONTENT \_ \_ PROTECTION \_ MANAGER de \_ \_ MF MEDIA ENGINE

Permite que el motor multimedia reprodgue contenido protegido.

## <a name="data-type"></a>Tipo de datos

**IUnknown\***

## <a name="remarks"></a>Observaciones

El valor de este atributo es un puntero a la [**interfaz IMFContentProtectionManager.**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) El autor de la llamada debe implementar la interfaz .

Este atributo puede ser uno de los atributos pasados [**a IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance). Es necesario si se va a reproducir contenido protegido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




