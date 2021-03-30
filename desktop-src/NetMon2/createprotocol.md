---
description: La función CreateProtocol notifica a Monitor de red que existe un analizador de protocolo específico.
ms.assetid: 13ae261f-b1c0-4afc-b718-d64b3d4ec5ee
title: Función CreateProtocol (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0b35f9505758256750ae02d24d6c2a84ed0646b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156704"
---
# <a name="createprotocol-function"></a>CreateProtocol función)

La función **CreateProtocol** notifica a monitor de red que existe un analizador de protocolo específico.

## <a name="syntax"></a>Sintaxis


```C++
HPROTOCOL WINAPI CreateProtocol(
  _In_ LPSTR         ProtocolName,
  _In_ LPENTRYPOINTS lpEntryPoints,
  _In_ DWORD         cbEntryPoints
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProtocolName* \[ de\]
</dt> <dd>

Nombre del protocolo que el analizador detectará.

</dd> <dt>

*lpEntryPoints* \[ de\]
</dt> <dd>

Una estructura [ENTRYPOINTS](entrypoints.md) que contiene los puntos de entrada del archivo DLL del analizador restantes. Vea la sección Comentarios para obtener una lista de las funciones de exportación a las que cada punto de entrada hace referencia. Los puntos de entrada se deben proporcionar en el orden especificado por la estructura **ENTRYPOINTS** .

</dd> <dt>

*cbEntryPoints* \[ de\]
</dt> <dd>

Tamaño de la estructura **ENTRYPOINTS** . Monitor de red proporciona una \_ macro de tamaño de ENTRYPOINTS que puede usar para especificar el tamaño de la estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un identificador del protocolo.

Si la función no se realiza correctamente, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

La DLL del analizador llama a **CreateProtocol** durante su implementación de [DllMain](dllmain-parser.md). Se llama a la función **CreateProtocol** cuando el sistema operativo carga el archivo DLL del analizador por primera vez.

Los puntos de entrada a los que se hace referencia en el parámetro *lpEntryPoints* incluyen punteros a las siguientes funciones de exportación que se deben proporcionar en el orden que se muestra aquí.

-   [Registro](register-parser.md)
-   [Eliminar registro](deregister.md)
-   [RecognizeFrame](recognizeframe.md)
-   [AttachProperties](attachproperties.md)
-   [FormatProperties](formatproperties.md)



| Para obtener información acerca de                                                                                 | Vea                                                     |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red.                                          | [Analizadores](parsers.md)                                  |
| Cómo implementar **DllMain** incluye un ejemplo de llamada a **CreateProtocol** dentro de **DllMain**. | [Implementar DllMain](implementing-dllmain-parser.md) |



 

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

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

