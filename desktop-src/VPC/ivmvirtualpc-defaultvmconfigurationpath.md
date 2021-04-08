---
title: Propiedad IVMVirtualPC DefaultVMConfigurationPath (VPCCOMInterfaces. h)
description: Directorio predeterminado en el que se buscarán los archivos de configuración de máquina virtual disponibles.
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- Propiedad DefaultVMConfigurationPath Virtual PC
- Propiedad DefaultVMConfigurationPath Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, propiedad DefaultVMConfigurationPath
topic_type:
- apiref
api_name:
- IVMVirtualPC.DefaultVMConfigurationPath
- IVMVirtualPC.get_DefaultVMConfigurationPath
- IVMVirtualPC.put_DefaultVMConfigurationPath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e13fc2323cb15bdbeb8c42e61810a376e49b3988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803199"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a>IVMVirtualPC::D propiedad efaultVMConfigurationPath

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera y establece el directorio predeterminado en el que se buscarán los archivos de configuración de máquina virtual disponibles.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica la ruta de acceso del directorio para los archivos de configuración de la máquina virtual predeterminada. En la cadena de ruta de acceso, una barra diagonal inversa ( \) puede aparecer inmediatamente antes del carácter nulo de terminación.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                               | Significado                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                                                 |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro *configurationPath* es **null**.<br/>                                                                                                |
| <dl> <dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)</dt> <dt>0x80070002</dt> </dl> | El sistema no puede encontrar el directorio especificado por el parámetro *configurationPath* .<br/>                                                          |
| <dl> <dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)</dt> <dt>0x80070003</dt> </dl> | El sistema no puede encontrar la ruta de acceso especificada por el parámetro *configurationPath* .<br/>                                                               |
| <dl> <dt>HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)</dt> <dt>0x8007007b</dt> </dl>    | El parámetro *configurationPath* contiene un carácter no válido (uno de los siguientes: " \* ? <>/ \| ": ").<br/>                                   |
| <dl> <dt>HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)</dt> <dt>0x800700a1</dt> </dl>    | El parámetro *configurationPath* especifica una ruta de acceso relativa o vacía. Se requiere una ruta de acceso absoluta.<br/>                                          |
| <dl> <dt>HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )</dt> <dt>0x8007006f</dt> </dl> | La ruta de acceso especificada por el parámetro *configurationPath* es demasiado larga. La longitud de la ruta de acceso debe ser menor que el número máximo de caracteres de **\_ ruta de acceso** (260).<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                                             |
| <dl> <dt>Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada</dt> <dt>0xA0040951</dt> </dl>     | El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).<br/>                                                          |



## <a name="remarks"></a>Observaciones

De forma predeterminada, este valor de propiedad se establece en el siguiente directorio: "% LocalAppData% \\ Microsoft \\ Windows Virtual PC \\ virtual machines \\ ".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

