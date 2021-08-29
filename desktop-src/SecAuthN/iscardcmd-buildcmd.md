---
description: Construye una unidad de datos de protocolo de aplicación de comandos (APDU) válida para la transmisión a una tarjeta inteligente.
ms.assetid: d1003cc3-c235-4635-ad5a-8cea7363bf30
title: Método ISCardCmd::BuildCmd (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.BuildCmd
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: aec07516a44dc06489a627c690ec15dd2e0a80edef9fee49801c0ed23d64439f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015265"
---
# <a name="iscardcmdbuildcmd-method"></a>Método ISCardCmd::BuildCmd

\[El **método BuildCmd** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método BuildCmd** construye una unidad de datos de [*protocolo*](../secgloss/a-gly.md) de aplicación de comandos (APDU) válida para la transmisión a una [*tarjeta inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BuildCmd(
  [in] BYTE         byClassId,
  [in] BYTE         byInsId,
  [in] BYTE         byP1,
  [in] BYTE         byP2,
  [in] LPBYTEBUFFER pbyData,
  [in] LONG         *p1Le
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byClassId* \[ En\]
</dt> <dd>

Identificador de clase de comando.

</dd> <dt>

*byInsId* \[ En\]
</dt> <dd>

Identificador de instrucción de comando.

</dd> <dt>

*byP1* \[ En\]
</dt> <dd>

Primer parámetro del comando.

</dd> <dt>

*byP2* \[ En\]
</dt> <dd>

Segundo parámetro del comando.

</dd> <dt>

*pbyData* \[ En\]
</dt> <dd>

Puntero a la parte de datos del comando.

</dd> <dt>

*p1Le* \[ En\]
</dt> <dd>

Puntero a un entero LONG que contiene la longitud esperada de los datos devueltos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno de los parámetros no es válido.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido.<br/>        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                      |



 

## <a name="remarks"></a>Comentarios

Para encapsular el comando en otro comando, llame a [**Encapsulate**](iscardcmd-encapsulate.md).

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo construir un comando APDU. En el ejemplo se supone que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) y que pIByteRequest es un puntero válido a una instancia de la interfaz [**IByteBuffer**](ibytebuffer.md) inicializada con una llamada anterior al método [**IByteBuffer::Initialize.**](ibytebuffer-initialize.md)


```C++
LONG       lLe = 0;
HRESULT    hr;

hr = pISCardCmd->BuildCmd(0x00,   // Some cards prefer 0xC0
                          0xa4,   // 'Select File'
                          0x00,
                          0x00,
                          pIByteRequest,
                          &lLe);
if (FAILED(hr))
{
    printf("Failed ISCardCmd::BuildCmd\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardCmd se define como \_ D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Encapsular**](iscardcmd-encapsulate.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
