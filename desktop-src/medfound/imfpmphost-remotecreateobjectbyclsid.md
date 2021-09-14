---
description: Versión remota del método IMFPMPHost::CreateObjectByCLSID.
ms.assetid: be96be6d-47de-4d2b-81fc-13079de33888
title: RemoteCreateObjectByCLSID (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e57307ece851484675d01a699037647efad771d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257916"
---
# <a name="remotecreateobjectbyclsid"></a>RemoteCreateObjectByCLSID

Versión remota del método [**IMFPMPHost::CreateObjectByCLSID.**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid)

``` syntax
[call_as(CreateObjectByCLSID)]
HRESULT RemoteCreateObjectByCLSID( 
    REFCLSID clsid,
    BYTE *pbData, 
    DWORD cbData, 
    REFIID riid,
    void **ppv
);
```

## <a name="remarks"></a>Observaciones

Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método. El método no aparece en la tabla virtual de la interfaz . Si se llama a [**CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) a través de los límites del proceso, el archivo DLL de proxy o código auxiliar de Media Foundation traduce la llamada en una llamada al método remoto y, a continuación, la vuelve a traducir.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mfuuid.lib</dt> </dl>                    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost)
</dt> <dt>

[Sesión multimedia de PMP](pmp-media-session.md)
</dt> <dt>

[Ruta de acceso de medios protegidos](protected-media-path.md)
</dt> </dl>

 

 




