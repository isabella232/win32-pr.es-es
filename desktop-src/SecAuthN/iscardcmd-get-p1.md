---
description: Recupera el primer byte del parámetro (P1) de la unidad de datos del protocolo de aplicación (APDU).
ms.assetid: a6648e70-96d8-4b7d-ae6d-8832e38d1c71
title: Método ISCardCmd::get_P1 (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 94fd7dbe7629ebc3137a6323515d401688dc489cf08c7bb3e6d4262527d4d0a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014965"
---
# <a name="iscardcmdget_p1-method"></a>Método ISCardCmd::get \_ P1

\[El **método \_ get P1** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método get \_ P1** recupera el primer byte de parámetro (P1) de la unidad [*de datos del protocolo de aplicación*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_P1(
  [out] BYTE *pbyP1
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbyP1* \[ out\]
</dt> <dd>

Puntero al byte P1 en la APDU a la devolución.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro pbyP1* no es válido.<br/>  |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido *en pbyP1.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                       |



 

## <a name="remarks"></a>Comentarios

Para establecer el parámetro P1 en un nuevo valor, llame a [**put \_ P1**](iscardcmd-put-p1.md).

Para obtener los parámetros P2 o P3, llame [**a get \_ P2**](iscardcmd-get-p2.md) [**y get \_ P3**](iscardcmd-get-p3.md) respectivamente.

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de [*error*](../secgloss/s-gly.md) de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo recuperar el primer byte de parámetro (P1) de la unidad [*de datos del protocolo de aplicación*](../secgloss/a-gly.md) (APDU). En el ejemplo se supone que pISCardCmd es un puntero válido a una instancia de la [**interfaz ISCardCmd.**](iscardcmd.md)


```C++
BYTE  byP1;
HRESULT  hr;

// Retrieve the P1 byte.
hr = pISCardCmd->get_P1(&byP1);
if (FAILED(hr))
{
  printf("Failed get_P1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardCmd se define como \_ D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**obtener \_ P2**](iscardcmd-get-p2.md)
</dt> <dt>

[**obtener \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ P1**](iscardcmd-put-p1.md)
</dt> </dl>

 

 
