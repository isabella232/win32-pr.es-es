---
description: La función AttachPropertyInstance asigna una propiedad existente a una ubicación específica de los datos reconocidos.
ms.assetid: b44cf8d1-939b-45da-8a9a-b4bdcf9faf43
title: Función AttachPropertyInstance (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 50ab07967605f8a24ba330a3cb13f80c833cf542
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069354"
---
# <a name="attachpropertyinstance-function"></a>Función AttachPropertyInstance

La **función AttachPropertyInstance** asigna una propiedad existente a una ubicación específica de los datos reconocidos.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI AttachPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ En\]
</dt> <dd>

Controle el marco que se está analizando. Use el identificador pasado al archivo DLL del analizador en el *parámetro hFrame* de la [**función AttachProperties.**](attachproperties.md)

</dd> <dt>

*hProperty* \[ En\]
</dt> <dd>

Identificador de una [**estructura PROPERTYINFO**](propertyinfo.md) que define la propiedad . Al implementar la función [**de exportación Register,**](register-parser.md) se especifica la **estructura PROPERTYINFO** que define la propiedad .

</dd> <dt>

*Longitud* \[ En\]
</dt> <dd>

Longitud de los datos de esta instancia de la propiedad .

</dd> <dt>

*lpData* \[ En\]
</dt> <dd>

Puntero a la ubicación en los datos reconocidos donde se encuentra el valor de propiedad. Use el puntero pasado al archivo DLL del analizador en el *parámetro lpProtocol* de la [**función AttachProperties.**](attachproperties.md)

</dd> <dt>

*HelpID* \[ En\]
</dt> <dd>

Identificador (de 0 a 2047) que se usa para establecer la Ayuda contextual para la propiedad .

El número de identificador es relativo al archivo de Ayuda asociado a la base de datos de [*propiedades de protocolo*](p.md).

</dd> <dt>

*IndentLevel* \[ En\]
</dt> <dd>

Nivel de sangría (de 0 a 15) utilizado para mostrar una propiedad jerárquicamente.

Monitor de red usa los niveles 0 a 14 para aplicar sangría a las propiedades. El nivel 15 es un valor especial que permite a un analizador adjuntar una propiedad oculta que no está visible.

</dd> <dt>

*IFlags* \[ En\]
</dt> <dd>

Valor de campo BIT que indica el orden de los BIT dentro de una propiedad. Los analizadores anteriores que *establecen fError* en 0 o 1 ahora deben establecer *fError* en IFLAG \_ ERROR. Establezca este parámetro en uno de los valores siguientes.



| Value                                                                                                                                                         | Significado                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <dt>**ERROR \_ DE IFLAG**</dt> </dl>       | Los datos del marco tienen un error.<br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <dt>**IFLAG \_ SWAPPED**</dt> </dl> | En el momento de la **asociación,** el byte WORD es un formato que no es Intel.<br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <dt>**IFLAG \_ UNICODE**</dt> </dl> | En el momento de la **asociación, STRING** es Unicode.<br/>               |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es **TRUE.**

Si la función no se realiza correctamente, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Observaciones

Se **llama a la función AttachPropertyInstance** durante la implementación de la función de exportación [**AttachProperties.**](attachproperties.md) Cuando se adjunta una propiedad a los datos, Monitor de red crea una [**estructura PROPERTYINST**](propertyinst.md) que define la instancia de la propiedad adjunta.

Durante la implementación de [**AttachProperties,**](attachproperties.md)llame **a AttachPropertyInstance** para usar los datos tal como existen en la captura. También puede llamar a la [**función AttachPropertyInstanceEx**](attachpropertyinstanceex.md) para modificar los datos de propiedad. Sin embargo, se recomienda usar los datos tal como existen en la captura.



| Para obtener información sobre                                        | Vea                                                                |
|-----------------------------------------------------------|--------------------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red. | [**Analizadores**](parsers.md)                                         |
| Cómo llamar a **AttachPropertyInstance**.                   | [Implementación de AttachProperties](implementing-attachproperties.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**AttachProperties**](attachproperties.md)
</dt> <dt>

[**AttachPropertyInstanceEx**](attachpropertyinstanceex.md)
</dt> <dt>

[**PROPERTYINST**](propertyinst.md)
</dt> </dl>

 

 




