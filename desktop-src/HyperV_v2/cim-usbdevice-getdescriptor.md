---
description: Devuelve el descriptor de USBDevice tal y como lo especifican los parámetros de entrada.
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
ms.openlocfilehash: f6aa8e7dc37f2bb7fe48ce0293bbaad9663150dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666904"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-hyper-v-management"></a>Método GetDescriptor de la clase CIM_USBDevice (administración de Hyper-V)

Devuelve el descriptor de USBDevice tal y como lo especifican los parámetros de entrada.

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

*RequestType* \[ de\]
</dt> <dd>

Mapa de bits que identifica el tipo de solicitud de descriptor y el destinatario. El tipo de solicitud puede ser ' Standard ', ' Class ' o ' specific Vendor '. El destinatario puede ser ' Device ', ' interface ', ' Endpoint ' u ' Other '. Consulte la especificación USB para ver los valores adecuados para cada bit.

</dd> <dt>

*RequestValue* \[ de\]
</dt> <dd>

Contiene el tipo de descriptor en el byte alto y el índice de descriptor (por ejemplo, índice o desplazamiento en la matriz de descriptores) en el byte bajo. Consulte la especificación de USB para obtener más información.

</dd> <dt>

*RequestIndex* \[ de\]
</dt> <dd>

Define el código de identificador de idioma de 2 bytes usado por USBDevice al devolver los datos del descriptor de cadena. El parámetro suele ser 0 para los descriptores que no son de cadena. Consulte la especificación de USB para obtener más información.

</dd> <dt>

*RequestLength* \[ in, out\]
</dt> <dd>

En la entrada, contiene la longitud (en octetos) del descriptor que se debe devolver. Si este valor es menor que la longitud real del descriptor, solo se devolverá la longitud solicitada. Si es mayor que la longitud real, se devuelve la longitud real. En la salida, este parámetro es la longitud, en octetos, del búfer que se va a devolver. Si el descriptor solicitado no existe, el contenido de este parámetro es indefinido.

</dd> <dt>

*Búfer* \[ de enuncia\]
</dt> <dd>

Devuelve la información de descriptor solicitada. Si el descriptor no existe, el contenido del parámetro es indefinido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_USBDEVICE CIM**](cim-usbdevice.md)
</dt> </dl>

 

 




