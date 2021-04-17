---
description: La función CreateHandoffTable crea una tabla de entrega que incluye la información del conjunto de entrega almacenada en el archivo INI del analizador.
ms.assetid: 6dbca2fa-33fb-48e8-b663-be59aec6264b
title: Función CreateHandoffTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 450bb4e4b158a937d48d753a5ff5c831f8fa58c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667119"
---
# <a name="createhandofftable-function"></a>CreateHandoffTable función)

La función **CreateHandoffTable** crea una [*tabla de entrega*](h.md) que incluye la información del conjunto de entrega almacenada en el archivo ini del analizador.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI CreateHandoffTable(
  _In_  LPSTR          secName,
  _In_  LPSTR          iniFile,
  _Out_ LPHANDOFFTABLE *hTable,
  _In_  DWORD          nMaxProtocolEntries,
  _In_  DWORD          base
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*secName* \[ de\]
</dt> <dd>

Cadena que indica la sección del archivo INI donde se encuentra la información del conjunto de entrega.

</dd> <dt>

*inifile* \[ de\]
</dt> <dd>

Cadena que incluye el nombre del archivo INI del analizador.

</dd> <dt>

*hTable* \[ enuncia\]
</dt> <dd>

Identificador de una estructura **HANDOFFTABLE** creada y mantenida por monitor de red.

</dd> <dt>

*nMaxProtocolEntries* \[ de\]
</dt> <dd>

Número que especifica el número máximo de entradas que puede procesar la tabla de entrega.

</dd> <dt>

*base* \[ de de\]
</dt> <dd>

Base numérica de los números de conjunto de entrega almacenados en el archivo INI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es el número de entradas de la tabla de entrega.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

La tabla de entrega creada por Monitor de red se basa en la información proporcionada en el INI del analizador. A continuación, el identificador devuelto para la tabla de entrega se puede usar para obtener un identificador de uno de los protocolos incluidos en la tabla. Para obtener un identificador de uno de estos protocolos, llame a [GetProtocolFromTable](getprotocolfromtable.md).

Tenga en cuenta que la aplicación de analizador nunca accede directamente a la estructura **HANDOFFTABLE** . Monitor de red crea y mantiene esta estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[GetProtocolFromTable](getprotocolfromtable.md)
</dt> <dt>

[HANDOFFTABLE](handofftable.md)
</dt> </dl>

 

 




