---
description: Establece el segundo byte de parámetro (P2) en la unidad de datos del protocolo de aplicación (APDU).
ms.assetid: 8d11b967-33cd-4bfa-b294-cc0c422cf6cf
title: Método ISCardCmd::p ut_P2 (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a66ef756d65e4cc011e6a5e4797a8ccae690dd404b6f25f1f9a7d3bbb2826069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014585"
---
# <a name="iscardcmdput_p2-method"></a>Método ISCardCmd::p ut \_ P2

\[El **método put \_ P2** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método put \_ P2** establece el segundo byte de parámetro (P2) en la unidad [*de datos del protocolo de aplicación*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_P2(
  [in] BYTE byP2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byP2* \[ En\]
</dt> <dd>

Byte que es el campo P2.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro byP2* no es válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                     |



 

## <a name="remarks"></a>Comentarios

Para establecer el valor P1 de la APDU, llame a [**put \_ P1**](iscardcmd-put-p1.md).

Para recuperar los valores P1, P2 y P3 existentes, llame a [**get \_ P1**](iscardcmd-get-p1.md), [**get \_ P2**](iscardcmd-get-p2.md) u [**get \_ P3**](iscardcmd-get-p3.md) respectivamente.

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de [*error*](../secgloss/s-gly.md) de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo establecer el segundo byte de parámetro (P2) de la unidad de [*datos del protocolo de aplicación*](../secgloss/a-gly.md) (APDU). En el ejemplo se supone que pISCardCmd es un puntero válido a una instancia de la [**interfaz ISCardCmd.**](iscardcmd.md)


```C++
HRESULT  hr;

// Set the P2 byte.
hr = pISCardCmd->put_P2(0x06);
if (FAILED(hr))
{
  printf("Failed put_P2\n");
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

[**obtener \_ P1**](iscardcmd-get-p1.md)
</dt> <dt>

[**obtener \_ P2**](iscardcmd-get-p2.md)
</dt> <dt>

[**obtener \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ P1**](iscardcmd-put-p1.md)
</dt> </dl>

 

 
