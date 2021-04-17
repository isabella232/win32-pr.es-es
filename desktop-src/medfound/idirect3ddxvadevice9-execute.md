---
description: Realiza una operación de descodificación de DirectX video Acceleration (DXVA).
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: 'IDirect3DDXVADevice9:: Execute (método) (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.Execute
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d624146c32b5f7eaeb4e680cf03878e8d065ee5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715887"
---
# <a name="idirect3ddxvadevice9execute-method"></a>IDirect3DDXVADevice9:: Execute (método)

Realiza una operación de descodificación de DirectX video Acceleration (DXVA).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Execute(
   DWORD          FunctionNum,
   VOID           *pInputData,
   DWORD          InputSize,
   VOID           *OutputData,
   DWORD          OutputSize,
   DWORD          NumBuffers,
   DXVABufferInfo *pBufferInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FunctionNum* 
</dt> <dd>

**DWORD** que contiene uno o más números de función de DXVA. Para obtener más información, consulte la [especificación de DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

</dd> <dt>

*pInputData* 
</dt> <dd>

Un puntero a un búfer que contiene los datos de entrada para la operación de descodificación. El significado de estos datos depende del tipo de superficie y el número de función.

</dd> <dt>

*Inlocate* 
</dt> <dd>

Tamaño de los datos de entrada, en bytes.

</dd> <dt>

*OutputData* 
</dt> <dd>

Puntero a un búfer en el que el acelerador de vídeo escribe los datos de salida.

</dd> <dt>

*Outlocate* 
</dt> <dd>

Tamaño del búfer de *OutputData* , en bytes.

</dd> <dt>

*NumBuffers* 
</dt> <dd>

Número de elementos de la matriz *pBufferInfo* .

</dd> <dt>

*pBufferInfo* 
</dt> <dd>

Puntero a una matriz de estructuras [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 
