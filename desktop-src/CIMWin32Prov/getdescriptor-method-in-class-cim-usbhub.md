---
description: El método GetDescriptor devuelve el descriptor de concentrador USB especificado por los parámetros de entrada.
ms.assetid: 0090da35-0de1-4ea5-b983-bd9bf9997009
ms.tgt_platform: multiple
title: Método GetDescriptor de la CIM_USBHub (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBHub.GetDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5253f0eae0acf8844e844f5bfb48fcd73b2b186c6537dfcfcb0da5fb8f46582f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879055"
---
# <a name="getdescriptor-method-of-the-cim_usbhub-class"></a>Método GetDescriptor de la clase \_ CIM USBHub

El **método GetDescriptor** devuelve el descriptor de concentrador USB especificado por los parámetros de entrada.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RequestType* \[ En\]
</dt> <dd>

Identificador asignado a bits para el tipo de solicitud de descriptor y el destinatario. Para obtener los valores adecuados para cada bit, consulte la especificación USB.

</dd> <dt>

*RequestValue* \[ En\]
</dt> <dd>

Contiene el tipo de descriptor en el byte alto y el índice del descriptor (por ejemplo, índice o desplazamiento en la matriz de descriptores) en el byte bajo. Para más información, consulte la especificación USB.

</dd> <dt>

*RequestIndex* \[ En\]
</dt> <dd>

Especifica el código de identificador de idioma de 2 bytes que usa el dispositivo USB al devolver datos del descriptor de cadena. El parámetro suele ser 0 (cero) para los descriptores que no son de cadena. Para más información, consulte la especificación USB.

</dd> <dt>

*RequestLength* \[ in, out\]
</dt> <dd>

En la entrada, la longitud (en octetos) del descriptor que se debe devolver. Si este valor es menor que la longitud real del descriptor, solo se devuelve la longitud solicitada. Si es mayor que la longitud real, se devuelve la longitud real.

En la salida, la longitud (en octetos) del búfer que se devuelve. Si el descriptor solicitado no existe, el contenido de este parámetro no está definido.

</dd> <dt>

*Búfer* \[ out\]
</dt> <dd>

Buffer devuelve la información de descriptor solicitada. Si el descriptor no existe, el contenido del búfer no está definido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el descriptor USB se devuelve correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error. En una subclase, el conjunto de códigos de retorno posibles se podría especificar mediante un **calificador ValueMap** en el método . Las cadenas a las que se traduce el contenido **mofqualifier** también se pueden especificar en la subclase como calificador de **matriz Values.**

## <a name="remarks"></a>Comentarios

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ USBHub**](getdescriptor-method-in-class-cim-usbhub.md)
</dt> <dt>

[**CIM \_ USBHub**](cim-usbhub.md)
</dt> </dl>

 

