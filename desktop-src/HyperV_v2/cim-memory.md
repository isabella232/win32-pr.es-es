---
description: Representa las funcionalidades y la administración de dispositivos lógicos relacionados con la memoria.
ms.assetid: 802c1c0e-7eab-4a17-9a29-6502ece6cb24
title: CIM_Memory (administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Volatile
- CIM_Memory.ErrorMethodology
- CIM_Memory.StartingAddress
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorInfo
- CIM_Memory.OtherErrorDescription
- CIM_Memory.CorrectableError
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorTransferSize
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorAddress
- CIM_Memory.SystemLevelAddress
- CIM_Memory.ErrorResolution
- CIM_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cdf896f03979770d31cdfcc5da7a2b324caf9936bb96114a2d1657e4b5a47e00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695305"
---
# <a name="cim_memory-class-hyper-v-management"></a>CIM_Memory (administración de Hyper-V)

Representa las funcionalidades y la administración de dispositivos lógicos relacionados con la memoria.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Memory"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
{
  boolean  Volatile;
  string   ErrorMethodology;
  uint64   StartingAddress;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a>Miembros

La **clase \_ Cim Memory** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Cim Memory** tiene estas propiedades.

<dl> <dt>

**AdditionalErrorData**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError.AdditionalErrorData"), **OctetString**, [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005.18", "MIF. Matriz de memoria física DMTF \| \| 001.13")
</dt> </dl>

Matriz de octetos que contiene información de error adicional. Un ejemplo es la eclocución de ECC o la devolución de los bits de comprobación si se usa una metodología de error basada en CRC. En el último caso, si se reconoce un error de un solo bit y se conoce el algoritmo CRC, es posible determinar el bit exacto que produjo el error.

Si la **propiedad ErrorInfo** contiene "3" (Aceptar), esta propiedad no se usa.

</dd> <dt>

**CorrectableError**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError.CorrectableError"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Matriz de memoria física DMTF \| \| 001.8")
</dt> </dl>

**True** si se puede corregir el error más reciente; de lo contrario, **false**. Si la **propiedad ErrorInfo** contiene "3" (Aceptar), esta propiedad no se usa.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Direcciones asignadas de matriz de memoria DMTF \| \| 001.4", "MIF. DMTF \| Memory Device Mapped Addresses \| 001.5"), **PUnit** ("byte \* 10^3")
</dt> </dl>

Dirección final a la que hace referencia una aplicación o sistema operativo y que asigna un controlador de memoria para el objeto de memoria. La dirección final se especifica en kilobytes.

</dd> <dt>

**ErrorAccess**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError.ErrorAccess"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Matriz de memoria física DMTF \| \| 001.10")
</dt> </dl>

Operación de acceso a memoria que produjo el último error. Si la **propiedad ErrorInfo** contiene "3" (Aceptar), esta propiedad no se usa.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

**Lectura** (3)


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

**Escritura** (4)


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

**Escritura parcial** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError.StartingAddress"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005.19", "MIF. Matriz de memoria física DMTF \| \| 001.14")
</dt> </dl>

Dirección del último error de memoria. La propiedad **ErrorInfo** describe el tipo de error. Si la **propiedad ErrorInfo** contiene "3" (Aceptar), esta propiedad no se usa.

</dd> <dt>

**ErrorData**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError.ErrorData"), **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Matriz de memoria física DMTF \| \| 001.12")
</dt> </dl>

Matriz que contiene los datos capturados durante el último acceso erróneo a la memoria. Los datos ocupan los primeros n octetos de la matriz necesarios para contener el número de bits especificado por la **propiedad ErrorTransferSize.**

Si la **propiedad ErrorTransferSize** contiene "0" (aceptar), esta propiedad no se usa.

</dd> <dt>

**ErrorDataOrder**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError.ErrorDataOrder")
</dt> </dl>

La ordenación de los datos almacenados en la **propiedad ErrorData.** Se puede especificar "Least Significant Byte First" (value=1) o "Most Significant Byte First" (2). Si la **propiedad ErrorTransferSize** contiene "0" (aceptar), esta propiedad no se usa.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

**Primer byte menos significativo** (1)


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

**Primer byte más significativo** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError.ErrorInfo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005.12", "MIF. DMTF \| Physical Memory Array \| 001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Memory**.**OtherErrorDescription**")
</dt> </dl>

Tipo del último error que se produce.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

**Aceptar** (3)


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

**Lectura no leída** (4)


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

**Error de paridad** (5)


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

**Error de un solo bit** (6)


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

**Error de doble bit** (7)


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

**Error de varios bits** (8)


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

**Error de nibble** (9)


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

**Error de suma de** comprobación (10)


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

**Error de CRC** (11)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Sin definir** (12)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Sin definir** (13)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Sin definir** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Matriz de memoria física DMTF \| \| 001.7")
</dt> </dl>

Indica si el objeto de memoria usa algoritmos de paridad, algoritmos CRC, ECC u otros mecanismos. También se pueden proporcionar detalles sobre el algoritmo.

</dd> <dt>

**ErrorResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError.ErrorResolution"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005.21", "MIF. Matriz de memoria física DMTF \| \| 001.15"), **PUnit** ("byte")
</dt> </dl>

Intervalo, en bytes, en el que se puede resolver el último error. Por ejemplo, si las direcciones de error se resuelven en el bit 11, como en una página típica; a continuación, los errores se pueden resolver en límites 4K y esta propiedad se establece en "4000". Si la **propiedad ErrorInfo** contiene "3" (Aceptar), esta propiedad no se usa.

</dd> <dt>

**ErrorTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError.ErrorTime")
</dt> </dl>

Hora a la que se produjo el último error de memoria. Si la **propiedad ErrorInfo** contiene "3" (Correcto), esta propiedad no se usa.

</dd> <dt>

**ErrorTransferSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError.ErrorTransferSize"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Matriz de memoria física DMTF \| \| 001.11"), **PUnit** ("bit")
</dt> </dl>

Tamaño de la transferencia de datos, en bits, que produjo el último error. "0" no indica ningún error. Si la **propiedad ErrorInfo** contiene "3" (Correcto), esta propiedad no se usa.

</dd> <dt>

**OtherErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError.OtherErrorDescription"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Memory**.**ErrorInfo**")
</dt> </dl>

Descripción del tipo de error, cuando la **propiedad ErrorType** se establece en "1" (otro).

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array Mapped Addresses \| 001.3", "MIF. Direcciones asignadas del dispositivo de memoria DMTF \| \| 001.4"), **PUnit** ("byte \* 10^3")
</dt> </dl>

Dirección inicial a la que hace referencia una aplicación o sistema operativo y que asigna un controlador de memoria para el objeto de memoria. La dirección inicial se especifica en kilobytes.

</dd> <dt>

**SystemLevelAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_MemoryError.SystemLevelAddress")
</dt> </dl>

**True** si la información de dirección de **la propiedad ErrorAddress** es una dirección de nivel de sistema, **false** si es una dirección física.

</dd> <dt>

**Volátil**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**True** si la memoria es volátil; de lo contrario, **false**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ StorageExtent**](cim-storageextent.md)
</dt> </dl>

 

