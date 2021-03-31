---
description: El método de autenticación de ICC \_ permite que una aplicación autentique la tarjeta inteligente.
ms.assetid: 98aea241-6bdc-4f47-b56c-a90f69fcd9a4
title: 'ISCardAuth:: ICC_Auth (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.ICC_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 015b5c395f025abea4ab2dc756c03691bbc27e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001090"
---
# <a name="iscardauthicc_auth-method"></a>ISCardAuth:: ICC ( \_ método de autenticación)

\[El método de **\_ autenticación de ICC** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método de **\_ autenticación de ICC** permite que una aplicación autentique la tarjeta inteligente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ICC_Auth(
  [in]      LONG         lAlgoID,
  [in]      LPBYTEBUFFER pParam,
  [in, out] LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lAlgoID* \[ de\]
</dt> <dd>

Algoritmo que se va a usar en el proceso de autenticación.

</dd> <dt>

*pParam* \[ de\]
</dt> <dd>

Un objeto [**IByteBuffer**](ibytebuffer.md) que contiene los parámetros específicos del proveedor del proceso de autenticación.

</dd> <dt>

*pBuffer* \[ in, out\]
</dt> <dd>

En la entrada, contiene los datos que se van a usar en el proceso de autenticación.

En la salida, contiene el resultado del proceso de autenticación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Observaciones

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardAuth**](iscardauth.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardAuth**](iscardauth.md)
</dt> </dl>

 

 
