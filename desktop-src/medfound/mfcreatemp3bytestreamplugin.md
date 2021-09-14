---
description: Crea un controlador de secuencia de bytes para el origen multimedia MP3.
ms.assetid: A213BAEF-D98F-485B-8840-BE131E9B26C0
title: Función MFCreateMP3ByteStreamPlugin
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateMP3ByteStreamPlugin
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0b8bcd153471ddd8acd648d5775b4dc964693a56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363867"
---
# <a name="mfcreatemp3bytestreamplugin-function"></a>Función MFCreateMP3ByteStreamPlugin

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, las aplicaciones deben usar [el solucionador de origen](source-resolver.md) para crear el origen multimedia MP3.\]

Crea un controlador de secuencia de bytes para el origen multimedia MP3.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT __stdcall MFCreateMP3ByteStreamPlugin(
  _In_  REFIID riid,
  _Out_ LPVOID *ppvHandler
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*riid* \[ En\]
</dt> <dd>

Identificador de interfaz (IID) de la interfaz solicitada. Establezca este parámetro en **IID \_ IMFByteStreamHandler para** recibir un puntero a la [**interfaz IMFByteStreamHandler.**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)

</dd> <dt>

*ppvHandler* \[ out\]
</dt> <dd>

Recibe un puntero a la interfaz . El autor de la llamada debe liberar la interfaz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Esta función no tiene ninguna biblioteca de importación asociada. Para llamar a esta función, debe usar las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a mf.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows Vista<br/>                             |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008<br/>                       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation Functions](media-foundation-functions.md)
</dt> <dt>

[Controladores de esquema y Byte-Stream controladores de esquema](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Solucionador de origen](source-resolver.md)
</dt> </dl>

 

 
