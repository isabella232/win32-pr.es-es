---
description: Devuelve el descriptor USBDevice especificado por los parámetros de entrada.
ms.assetid: 89bb8a49-6fca-422c-808d-70ae77aae4c3
title: Método GetDescriptor de la clase CIM_USBDevice (administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice.GetDescriptor
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d0523cc88205792f9429eb1a214d8b74a1ca4c2f2bf35813c25614f9f3c06199
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980785"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-hyper-v-management"></a>Método GetDescriptor de la clase CIM_USBDevice (administración de Hyper-V)

Devuelve el descriptor USBDevice especificado por los parámetros de entrada.

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

Mapa de bits que identifica el tipo de solicitud de descriptor y el destinatario. El tipo de solicitud puede ser "standard", "class" o "vendor-specific". El destinatario puede ser "dispositivo", "interfaz", "punto de conexión" u "otro". Consulte la especificación USB para obtener los valores adecuados para cada bit.

</dd> <dt>

*RequestValue* \[ En\]
</dt> <dd>

Contiene el tipo de descriptor en el byte alto y el índice del descriptor (por ejemplo, índice o desplazamiento en la matriz descriptor) en el byte bajo. Consulte la especificación USB para obtener más información.

</dd> <dt>

*RequestIndex* \[ En\]
</dt> <dd>

Define el código de identificador de idioma de 2 bytes usado por USBDevice al devolver datos del descriptor de cadena. El parámetro suele ser 0 para descriptores que no son de cadena. Consulte la especificación USB para obtener más información.

</dd> <dt>

*RequestLength* \[ in, out\]
</dt> <dd>

En la entrada, contiene la longitud (en octetos) del descriptor que se debe devolver. Si este valor es menor que la longitud real del descriptor, solo se devolverá la longitud solicitada. Si es mayor que la longitud real, se devuelve la longitud real. En la salida, este parámetro es la longitud, en octetos, del búfer que se devuelve. Si el descriptor solicitado no existe, el contenido de este parámetro no está definido.

</dd> <dt>

*Búfer* \[ out\]
</dt> <dd>

Devuelve la información del descriptor solicitada. Si el descriptor no existe, el contenido del parámetro no está definido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ USBDevice**](cim-usbdevice.md)
</dt> </dl>

 

 




