---
description: Construye una unidad de datos de protocolo de aplicación de comandos (APDU) válida para la transmisión a una tarjeta inteligente.
ms.assetid: d1003cc3-c235-4635-ad5a-8cea7363bf30
title: 'ISCardCmd:: BuildCmd (método) (Scarddat. h)'
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
ms.openlocfilehash: f44597ea087f7ccec191abc9dd03787780e88b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277974"
---
# <a name="iscardcmdbuildcmd-method"></a>ISCardCmd:: BuildCmd (método)

\[El método **BuildCmd** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **BuildCmd** crea una [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) de comandos (APDU) válida para la transmisión a una [*tarjeta inteligente*](../secgloss/s-gly.md).

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

*byClassId* \[ de\]
</dt> <dd>

Identificador de clase de comando.

</dd> <dt>

*byInsId* \[ de\]
</dt> <dd>

Identificador de instrucción de comando.

</dd> <dt>

*byP1* \[ de\]
</dt> <dd>

Primer parámetro del comando.

</dd> <dt>

*byP2* \[ de\]
</dt> <dd>

Segundo parámetro del comando.

</dd> <dt>

*pbyData* \[ de\]
</dt> <dd>

Puntero a la parte de datos del comando.

</dd> <dt>

*p1Le* \[ de\]
</dt> <dd>

Puntero a un entero largo que contiene la longitud esperada de los datos devueltos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno de los parámetros no es válido.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido.<br/>        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                      |



 

## <a name="remarks"></a>Observaciones

Para encapsular el comando en otro comando, llame a [**Encapsulate**](iscardcmd-encapsulate.md).

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo construir una APDU de comando. En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) y que pIByteRequest es un puntero válido a una instancia de la interfaz [**IByteBuffer**](ibytebuffer.md) inicializada con una llamada anterior al método [**IByteBuffer:: Initialize**](ibytebuffer-initialize.md) .


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Encapsular**](iscardcmd-encapsulate.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
