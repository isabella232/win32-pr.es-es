---
description: El método GetChallenge devuelve un desafío de la tarjeta inteligente.
ms.assetid: a114ebfd-831f-4c6b-8156-ce631a732c9b
title: Método ISCardAuth::GetChallenge
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.GetChallenge
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0132ab8b4b3b2f646639c1618a9f2ca7e67fad1ce2c2fcec38590c7608802091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015425"
---
# <a name="iscardauthgetchallenge-method"></a>Método ISCardAuth::GetChallenge

\[El **método GetChallenge** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método GetChallenge** devuelve un desafío de la [*tarjeta inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetChallenge(
  [in, optional] LONG         lAlgoID,
  [in]           LONG         lLengthOfChallenge,
  [in]           LPBYTEBUFFER pParam,
  [in, out]      LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lAlgoID* \[ in, opcional\]
</dt> <dd>

Algoritmo que se va a usar en el proceso de autenticación.

</dd> <dt>

*lLengthOfChallenge* \[ En\]
</dt> <dd>

Longitud máxima de la respuesta esperada.

</dd> <dt>

*pParam* \[ En\]
</dt> <dd>

Objeto [**IByteBuffer**](ibytebuffer.md) que contiene parámetros específicos del proveedor del proceso de autenticación.

</dd> <dt>

*pBuffer* \[ in, out\]
</dt> <dd>

En la entrada, apunta al búfer.

En la salida, contiene los datos de desafío de la tarjeta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Comentarios

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardAuth**](iscardauth.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardAuth**](iscardauth.md)
</dt> </dl>

 

 
