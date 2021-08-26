---
description: El método app \_ Auth autentica la aplicación. Permite que una aplicación se autentique a sí misma (mediante un protocolo de desafío o firma) cuando una tarjeta inteligente solicita la autenticación.
ms.assetid: 0b86ce09-ca17-4d74-bc14-46b17262e669
title: Método ISCardAuth::APP_Auth
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.APP_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: db6d2b673caf15d5d15e63894a6c5a589fd2d18ea031a3201a562f255ee6cf2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015555"
---
# <a name="iscardauthapp_auth-method"></a>Método ISCardAuth::APP \_ Auth

\[El **método \_ app auth** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método app \_ Auth** autentica la aplicación. Permite que una aplicación se autentique a sí misma (mediante un protocolo de desafío o firma) cuando una tarjeta inteligente solicita la [*autenticación.*](../secgloss/s-gly.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT APP_Auth(
  [in] LONG         lAlgoID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lAlgoID* \[ En\]
</dt> <dd>

Algoritmo que se va a usar en el proceso de autenticación.

</dd> <dt>

*pParam* \[ En\]
</dt> <dd>

Un [**IByteBuffer que**](ibytebuffer.md) contiene parámetros específicos del proveedor del proceso de autenticación.

</dd> <dt>

*pBuffer* \[ En\]
</dt> <dd>

Datos necesarios para el cálculo.

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
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardAuth**](iscardauth.md)
</dt> <dt>

[**IByteBuffer**](ibytebuffer.md)
</dt> </dl>

 

 
