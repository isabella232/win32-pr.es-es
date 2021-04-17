---
description: El método GetDescriptor devuelve el descriptor de dispositivo USB según lo especificado por los parámetros de entrada.
ms.assetid: 5f36ac8a-e751-4494-b91e-c6733bc3e349
ms.tgt_platform: multiple
title: Método GetDescriptor de la clase CIM_USBDevice (Wmcodecdsp. h)
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
- CIMWin32.dll
ms.openlocfilehash: 35ce9a83efb580d6e5e44f55a01182e7390c120e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659480"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-wmcodecdsph"></a>Método GetDescriptor de la clase CIM_USBDevice (Wmcodecdsp. h)

El método **GetDescriptor** devuelve el descriptor de dispositivo USB según lo especificado por los parámetros de entrada.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

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

Identificador de asignación de bits para el tipo de solicitud de descriptor y el destinatario. Consulte la especificación USB para ver los valores adecuados para cada bit.

</dd> <dt>

*RequestValue* \[ de\]
</dt> <dd>

Contiene el tipo de descriptor en el byte alto y el índice de descriptor (por ejemplo, índice o desplazamiento en la matriz de descriptores) en el byte bajo. Para obtener más información, consulte la especificación USB.

</dd> <dt>

*RequestIndex* \[ de\]
</dt> <dd>

Especifica el código de identificador de idioma de 2 bytes utilizado por el dispositivo USB al devolver los datos del descriptor de cadena. El parámetro suele ser 0 (cero) para los descriptores que no son de cadena. Para obtener más información, consulte la especificación USB.

</dd> <dt>

*RequestLength* \[ in, out\]
</dt> <dd>

En la entrada, la longitud (en octetos) del descriptor que se debe devolver. Si este valor es menor que la longitud real del descriptor, solo se devuelve la longitud solicitada. Si es mayor que la longitud real, se devuelve la longitud real.

En la salida, la longitud (en octetos) del búfer que se va a devolver. Si el descriptor solicitado no existe, el contenido de este parámetro es indefinido.

</dd> <dt>

*Búfer* \[ de enuncia\]
</dt> <dd>

Devuelve la información de descriptor solicitada. Si el descriptor no existe, el contenido de este parámetro es indefinido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el descriptor USB se devuelve correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error. En una subclase, el conjunto de códigos de retorno posibles puede especificarse mediante un calificador **ValueMap** en el método. Las cadenas a las que se traduce el contenido de mofqualifier también se pueden especificar en la subclase como calificador de matriz de **valores** .

## <a name="remarks"></a>Observaciones

Este método no está implementado actualmente por WMI. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_USBDEVICE CIM**](getdescriptor-method-in-class-cim-usbdevice.md)
</dt> <dt>

[**\_USBDEVICE CIM**](cim-usbdevice.md)
</dt> </dl>

 

