---
description: Establece el identificador de instrucción especificado en la unidad de datos del protocolo de aplicación (APDU).
ms.assetid: ea527ffd-b053-467d-883d-b93d5bbfb071
title: Método ISCardCmd::p ut_InstructionId (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_InstructionId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7c9c5653bb4d6832161f313b924ba5c1a4f3d80c89ead48f19439935b534b259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577365"
---
# <a name="iscardcmdput_instructionid-method"></a>Método ISCardCmd::p ut \_ InstructionId

\[El **método put \_ InstructionId** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método put \_ InstructionId** establece el identificador de instrucción especificado en la unidad [*de datos del protocolo de aplicación*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_InstructionId(
  [in] BYTE byIns
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byIns* \[ En\]
</dt> <dd>

Byte que es el identificador de instrucción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro byIns* no es válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                      |



 

## <a name="remarks"></a>Comentarios

Para obtener el identificador de instrucción existente, llame [**a get \_ InstructionId**](iscardcmd-get-instructionid.md).

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de [*error*](../secgloss/s-gly.md) de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo establecer un identificador de instrucción en la unidad [*de datos del protocolo de aplicación*](../secgloss/a-gly.md) (APDU). En el ejemplo se supone que pISCardCmd es un puntero válido a una instancia de la [**interfaz ISCardCmd.**](iscardcmd.md)


```C++
HRESULT hr;

// Set the instruction ID.
hr = pISCardCmd->put_InstructionId(0xb2);
if (FAILED(hr))
{
  printf("Failed put_InstructionId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**get \_ InstructionId**](iscardcmd-get-instructionid.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
