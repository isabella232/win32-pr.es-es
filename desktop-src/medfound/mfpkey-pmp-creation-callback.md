---
description: Establece una devolución de llamada que crea la sesión de medios de PMP durante la resolución del origen.
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: Propiedad MFPKEY_PMP_Creation_Callback (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b18e04a15e035a9e4dc04a4039ce230342031a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276308"
---
# <a name="mfpkey_pmp_creation_callback-property"></a>\_Propiedad de \_ devolución de llamada de creación de MFPKEY PMP \_

Establece una devolución de llamada que crea la [sesión de medios de PMP](pmp-media-session.md) durante la resolución del origen.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**IUnknown \** _

VT \_ desconocido

_ *punkVal**



## <a name="remarks"></a>Observaciones

Algunos contenidos protegidos pueden requerir el uso de esta propiedad. Si es así, se produce un error en el proceso de resolución de origen con el código de error **MF \_ E la \_ resolución \_ requiere una devolución de llamada de \_ \_ creación \_ de PMP**.

Para usar esta propiedad, haga lo siguiente.

1.  Llame a [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) para crear un almacén de propiedades.
2.  Implemente la interfaz de devolución de llamada [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
3.  Establezca la \_ \_ \_ propiedad de devolución de llamada de creación de MFPKEY PMP en el almacén de propiedades. El valor es un puntero a la implementación de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
4.  Llame a [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl). Pase un puntero al almacén de propiedades en el parámetro *pProps* .

En el método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) de la interfaz de devolución de llamada, haga lo siguiente.

1.  Llame a [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) para crear la [sesión de medios de PMP](pmp-media-session.md).
2.  Llame a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en la sesión de medios de PMP a un puntero a la interfaz [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) .
3.  Llame a [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) en el objeto de resultado que se pasa en el parámetro *pAsyncResult* de [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Consulte el puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) devuelto para la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
4.  Llame a [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) con los parámetros siguientes:
    -   *dwQueue*: **\_ estándar de \_ cola \_ de devolución de llamada MFASYNC**
    -   *pCallback*: el puntero [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) obtenido en el paso 3.
    -   *pState*: el puntero [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) obtenido en el paso 2.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Sesión de medios de PMP](pmp-media-session.md)
</dt> <dt>

[Ruta de acceso a medios protegidos](protected-media-path.md)
</dt> <dt>

[Solucionador de origen](source-resolver.md)
</dt> </dl>

 

 
