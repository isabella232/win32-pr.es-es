---
description: La función de exportación AttachProperties asigna las propiedades a una ubicación dentro de una parte de datos reconocidos. AttachProperties debe implementarse para cada analizador que admita el archivo DLL del analizador.
ms.assetid: ef28f571-8364-47d0-841c-580e89333afd
title: Función de devolución de llamada AttachProperties (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 3b3cb4be93b8d960b39f0f5c5cf2b5a4809573cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677740"
---
# <a name="attachproperties-callback-function"></a>Función de devolución de llamada AttachProperties

La función de exportación **AttachProperties** asigna las propiedades a una ubicación dentro de una parte de datos reconocidos. **AttachProperties** debe implementarse para cada analizador que admita el archivo DLL del analizador.

## <a name="syntax"></a>Sintaxis


```C++
DWORD AttachProperties(
  _In_ HFRAME    hFrame,
  _In_ LPBYTE    lpFrame,
  _In_ LPBYTE    lpProtocol,
  _In_ DWORD     MacType,
  _In_ DWORD     BytesLeft,
  _In_ HPROTOCOL hPreviousProtocol,
  _In_ DWORD     nPreviousProtocolOffset,
  _In_ DWORD     lpInstData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ de\]
</dt> <dd>

Identificador del marco que se está analizando.

</dd> <dt>

*lpFrame* \[ de\]
</dt> <dd>

Puntero al primer byte de un marco.

</dd> <dt>

*lpProtocol* \[ de\]
</dt> <dd>

Puntero al principio de los datos reconocidos.

</dd> <dt>

*MacType* \[ de\]
</dt> <dd>

Valor MAC del primer protocolo en un marco. *MacType* puede ser uno de los siguientes:



| Value                                                                                                                                                                         | Significado                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**\_Ethernet de tipo Mac \_**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**\_TOKENRING de tipo Mac \_**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**\_FDDI de tipo Mac \_**</dt> </dl>                | ANSI X3T 9.5 <br/> |



 

</dd> <dt>

*BytesLeft* \[ de\]
</dt> <dd>

El número restante de bytes en un marco que empieza al principio de los datos reconocidos.

</dd> <dt>

*hPreviousProtocol* \[ de\]
</dt> <dd>

Identificador del protocolo anterior.

</dd> <dt>

*nPreviousProtocolOffset* \[ de\]
</dt> <dd>

Desplazamiento del protocolo anterior a partir del principio del marco.

</dd> <dt>

*lpInstData* \[ de\]
</dt> <dd>

Puntero a los datos de instancia proporcionados por el protocolo anterior. Los datos de instancia no pueden tener más de una \_ longitud de DWORD PTR.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es un puntero al primer byte después de los datos reconocidos en un marco o **null** si los datos reconocidos son la última parte de los datos de un marco.

Si la función no es correcta, el valor devuelto es un puntero a los datos reconocidos. El parámetro *lpProtocol* pasa el puntero a la dll del analizador.

## <a name="remarks"></a>Observaciones

Monitor de red llama a la función **AttachProperties** para cada analizador que reconoce un fragmento de datos en un marco. Tenga en cuenta que el analizador determina qué propiedades existen en los datos reconocidos y dónde se encuentra cada propiedad.

Durante la implementación de **AttachProperties**, llame a [AttachPropertyInstance](attachpropertyinstance.md) para usar los datos tal como existen en la captura. También puede llamar a la función [AttachPropertyInstanceEx](attachpropertyinstanceex.md) para modificar los datos de la propiedad. Sin embargo, se recomienda que use los datos tal como existen en la captura.

Solo se llama a las funciones **AttachPropertyInstanceEx** y **AttachPropertyInstance** para las propiedades que existen en los datos reconocidos. Tenga en cuenta que Monitor de red tiene una [*base de datos de propiedades*](p.md) para el analizador que contiene una descripción de todas las propiedades que admite el analizador.

**Datos de instancia**

Los datos de instancia son información que se pasa de un analizador a otro. Los datos de instancia pueden ser cualquier dato que sea menor o igual que \_ la longitud de un valor DWORD PTR, o un puntero a los datos, como los datos de fotogramas sin formato, que no es necesario que el analizador asigne o libere. En el parámetro *lpInstData* de las funciones **AttachProperties** y [RecognizeFrame](recognizeframe.md) , monitor de red proporciona un puntero a los datos de instancia del protocolo anterior. Puede establecer los datos de instancia para el analizador durante la implementación de **RecognizeFrame**.



| Para obtener información acerca de                                          | Vea                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red.   | [Analizadores](parsers.md)                                             |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.           | [Arquitectura de DLL de analizador](parser-dll-architecture.md)             |
| Cómo reconocer los datos.                                      | [Implementación de RecognizeFrame](implementing-recognizeframe.md)     |
| Cómo crear una base de datos de propiedades.                          | [Implementación del registro](implementing-register.md)                 |
| Cómo implementar **AttachProperties**  incluye un ejemplo. | [Implementación de AttachProperties](implementing-attachproperties.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[AttachPropertyInstance](attachpropertyinstance.md)
</dt> <dt>

[AttachPropertyInstanceEx](attachpropertyinstanceex.md)
</dt> <dt>

[RecognizeFrame](recognizeframe.md)
</dt> </dl>

 

 




