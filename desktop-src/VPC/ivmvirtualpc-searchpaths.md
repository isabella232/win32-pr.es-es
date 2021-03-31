---
title: Propiedad IVMVirtualPC SearchPaths (VPCCOMInterfaces. h)
description: Rutas de acceso del sistema de archivos que se usan para buscar archivos asociados a Windows Virtual PC.
ms.assetid: 2a2deee5-7e6b-4b90-8ce9-0b0dbeef0f30
keywords:
- Propiedad SearchPaths Virtual PC
- Propiedad SearchPaths Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, propiedad SearchPaths
topic_type:
- apiref
api_name:
- IVMVirtualPC.SearchPaths
- IVMVirtualPC.get_SearchPaths
- IVMVirtualPC.put_SearchPaths
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287eb07bc9205f9b6f0851bd8809f9a49dcf3242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800961"
---
# <a name="ivmvirtualpcsearchpaths-property"></a>IVMVirtualPC:: SearchPaths (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera y establece las rutas de acceso del sistema de archivos que se usan para buscar archivos asociados a Windows Virtual PC.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_SearchPaths(
  [in]          VARIANT searchPaths
);

HRESULT get_SearchPaths(
  [out, retval] VARIANT *searchPaths
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica una matriz SafeArray que contiene una ruta de acceso del sistema de archivos para cada entrada.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                               | Significado                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                               |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro es **null**.<br/>                                                                                                  |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                                 | El parámetro *searchPaths* no es válido y no se pudo analizar en una matriz de rutas de acceso.<br/>                                    |
| <dl> <dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)</dt> <dt>0x80070002</dt> </dl> | El sistema no puede encontrar un directorio especificado en el parámetro *searchPaths* .<br/>                                                |
| <dl> <dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)</dt> <dt>0x80070003</dt> </dl> | El sistema no puede encontrar una ruta de acceso especificada por el parámetro *searchPaths* .<br/>                                                     |
| <dl> <dt>HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)</dt> <dt>0x8007007b</dt> </dl>    | Una ruta de acceso especificada en el parámetro *searchPaths* contiene caracteres no válidos. Los caracteres no válidos son " \* ? <>/ \| ": ".<br/> |
| <dl> <dt>HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)</dt> <dt>0x800700a1</dt> </dl>    | Una ruta de acceso contenida en el parámetro *searchPaths* especifica una ruta de acceso relativa o vacía. Se requiere una ruta de acceso absoluta.<br/>          |
| <dl> <dt>HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )</dt> <dt>0x8007006f</dt> </dl> | La ruta de acceso especificada en el parámetro *searchPaths* es demasiado larga. La longitud de la ruta de acceso debe ser inferior a 260 caracteres.<br/>     |
| <dl> <dt>Máquina virtual \_ E \_ Pref \_ not \_ found</dt> <dt>0xA0040300</dt> </dl>                       | No se encontró la preferencia.<br/>                                                                                               |
| <dl> <dt>Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada</dt> <dt>0xA0040951</dt> </dl>     | El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).<br/>                                        |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                           |



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

 

