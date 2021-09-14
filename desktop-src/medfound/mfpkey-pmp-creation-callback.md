---
description: Establece una devolución de llamada que crea la sesión multimedia de PMP durante la resolución de origen.
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: MFPKEY_PMP_Creation_Callback propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b18e04a15e035a9e4dc04a4039ce230342031a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268831"
---
# <a name="mfpkey_pmp_creation_callback-property"></a>Propiedad MFPKEY \_ PMP \_ Creation \_ Callback

Establece una devolución de llamada que crea la [sesión multimedia de PMP durante](pmp-media-session.md) la resolución de origen.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**IUnknown\***

VT \_ UNKNOWN

**yaldaVal**



## <a name="remarks"></a>Observaciones

Es posible que algún contenido protegido requiera el uso de esta propiedad. Si es así, se produce un error en el proceso de resolución de código fuente con el código de error **MF E RESOLUTION REQUIRES \_ \_ \_ \_ PMP CREATION \_ \_ CALLBACK**.

Para usar esta propiedad, haga lo siguiente.

1.  Llame [**a PSCreateMemoryPropertyStore para**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) crear un almacén de propiedades.
2.  Implemente la [**interfaz de devolución de llamada DEVOLUCIÓN DE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) LLAMADA DE LA DEVOLUCIÓN DE LLAMADA DE LA DEVOLUCIÓN DE LLAMADA.
3.  Establezca la propiedad MFPKEY \_ PMP \_ Creation \_ Callback en el almacén de propiedades. El valor es un puntero a la [**implementación DE DEVOLUCIÓNASYNCASYNC.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
4.  Llame [**a CARDINALSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl). Pase un puntero al almacén de propiedades en el *parámetro pProps.*

En el [**método IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) de la interfaz de devolución de llamada, haga lo siguiente.

1.  Llame [**a MFCreatePMPMediaSession para**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) crear la sesión multimedia de [PMP](pmp-media-session.md).
2.  Llame [**a IMFGetService::GetService en**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) la sesión multimedia de PMP a un puntero a la interfaz [**DEFMPHost.**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost)
3.  Llame [**a IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) en el objeto de resultado que se pasa en el *parámetro pAsyncResult* de [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Consulte el puntero [**IUnknown devuelto**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para la [**interfaz IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
4.  Llame [**a MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) con los parámetros siguientes:
    -   *dwQueue:* **MFASYNC \_ CALLBACK \_ QUEUE \_ STANDARD**
    -   *pCallback:* el puntero DE DEvolución DE LLAMADA [**DE LA DEVOLUCIÓN DE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) LLAMADA OBTENIDO EN EL PASO 3.
    -   *pState:* el [**puntero DE LA PROPIEDAD DEMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) obtenido en el paso 2.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Sesión multimedia de PMP](pmp-media-session.md)
</dt> <dt>

[Ruta de acceso multimedia protegida](protected-media-path.md)
</dt> <dt>

[Solucionador de origen](source-resolver.md)
</dt> </dl>

 

 
