---
description: Función de proxy para el método InitializeFromMemory.
ms.assetid: d98fe40c-c3f1-4c46-a558-1910e3dee51b
title: IWICColorContext_InitializeFromMemory_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorContext_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 32c3c24902b6c3157b9776d84c5a8eea47cce43e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706492"
---
# <a name="iwiccolorcontext_initializefrommemory_proxy-function"></a>IWICColorContext \_ InitializeFromMemory \_ función proxy

Función de proxy para el método [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICColorContext_InitializeFromMemory_Proxy(
  _In_       IWICColorContext *THIS_PTR,
  _In_ const BYTE             *pbBuffer,
  _In_       UINT             cbBufferSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Este \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) \** _

</dd> <dt>

_pbBuffer * \[ en\]
</dt> <dd>

Tipo: **const byte \** _

Búfer que se usa para inicializar [_ *IWICColorContext* *](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).

</dd> <dt>

*cbBufferSize* \[ de\]
</dt> <dd>

Tipo: **uint**

Tamaño del búfer de *pbBuffer* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




