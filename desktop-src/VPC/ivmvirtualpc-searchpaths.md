---
title: Propiedad IVMVirtualPC SearchPaths (VPCCOMInterfaces.h)
description: Rutas de acceso del sistema de archivos que se usan para buscar archivos asociados a Windows Virtual PC.
ms.assetid: 2a2deee5-7e6b-4b90-8ce9-0b0dbeef0f30
keywords:
- Equipo virtual de la propiedad SearchPaths
- Propiedad SearchPaths Virtual PC , interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , propiedad SearchPaths
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
ms.openlocfilehash: ac4ef75bf0a696494b839f330063ca310927a0d796829d96575721f492b8b691
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471255"
---
# <a name="ivmvirtualpcsearchpaths-property"></a>IVMVirtualPC::SearchPaths, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

Especifica una safearray que contiene una ruta de acceso del sistema de archivos para cada entrada.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                               | Significado                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                               |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro es **NULL.**<br/>                                                                                                  |
| <dl> <dt>E \_ Invalidarg</dt> <dt>0x80000003</dt> </dl>                                 | El *parámetro searchPaths* no es válido y no se pudo analizar en una matriz de rutas de acceso.<br/>                                    |
| <dl> <dt>HRESULT \_ DESDE \_ WIN32 (ARCHIVO DE ERROR \_ \_ NO \_ ENCONTRADO)</dt> <dt>0X80070002</dt> </dl> | El sistema no puede encontrar un directorio especificado en el *parámetro searchPaths.*<br/>                                                |
| <dl> <dt>HRESULT \_ DESDE \_ WIN32 (RUTA DE ACCESO DE ERROR \_ \_ NO \_ ENCONTRADA)</dt> <dt>0X80070003</dt> </dl> | El sistema no puede encontrar una ruta de acceso especificada por el *parámetro searchPaths.*<br/>                                                     |
| <dl> <dt>HRESULT \_ DESDE \_ WIN32(ERROR \_ INVALID \_ NAME) 0X8007007B</dt> <dt></dt> </dl>    | Una ruta de acceso especificada en el *parámetro searchPaths* contiene caracteres no válidos. Los caracteres no válidos son " \* ?<>/ \| ":".<br/> |
| <dl> <dt>HRESULT \_ DESDE \_ WIN32(ERROR \_ BAD \_ PATHNAME)</dt> <dt>0X800700A1</dt> </dl>    | Una ruta de acceso contenida en el *parámetro searchPaths* especifica una ruta de acceso vacía o relativa. Se requiere una ruta de acceso absoluta.<br/>          |
| <dl> <dt>HRESULT \_ DESDE \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)</dt> <dt>0x8007006f</dt> </dl> | La ruta de acceso especificada en el *parámetro searchPaths* es demasiado larga. La longitud de la ruta de acceso debe tener menos de 260 caracteres.<br/>     |
| <dl> <dt>Máquina virtual \_ E \_ NO SE ENCONTRÓ \_ LA \_ </dt> <dt>0XA0040300</dt> </dl>                       | No se encontró la preferencia.<br/>                                                                                               |
| <dl> <dt>Máquina virtual \_ E \_ HARDWARE VIRTUALIZATION DISABLED \_ \_ 0xA0040951</dt> <dt></dt> </dl>     | El procesador no admite extensiones de Virtualización acelerada por hardware (HAV).<br/>                                        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Product<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

