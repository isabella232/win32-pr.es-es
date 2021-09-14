---
description: Inicia una carga de datos de un solo elemento desde el autor de la llamada.
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: Método IWiaTransfer::Upload (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Upload
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6aae6ca8f86d07ec052fdd59d24b0da2b96599d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362806"
---
# <a name="iwiatransferupload-method"></a>IWiaTransfer::Upload método

Inicia una carga de datos de un solo elemento desde el autor de la llamada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Upload(
  [in] LONG                 lFlags,
  [in] IStream              *pSource,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*pSource* \[ En\]
</dt> <dd>

Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\***

Especifica un puntero a los [datos de IStream.](/windows/win32/api/objidl/nn-objidl-istream)

</dd> <dt>

*pIWiaTransferCallback* \[ En\]
</dt> <dd>

Tipo: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

Especifica un puntero a la interfaz [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) del autor de la llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
