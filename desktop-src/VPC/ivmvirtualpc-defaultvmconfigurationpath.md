---
title: Propiedad IVMVirtualPC DefaultVMConfigurationPath (VPCCOMInterfaces.h)
description: Directorio predeterminado en el que se buscarán los archivos de configuración de máquina virtual disponibles.
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- Equipo virtual de la propiedad DefaultVMConfigurationPath
- Propiedad DefaultVMConfigurationPath De PC virtual, interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , Propiedad DefaultVMConfigurationPath
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
ms.openlocfilehash: 09f6370dfb868ec386e05f361240a74412f13a7d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387641"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a>IVMVirtualPC::D efaultVMConfigurationPath

\[Windows Virtual PC ya no está disponible para su uso a Windows 8. En su lugar, use el proveedor WMI de [Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

Especifica la ruta de acceso del directorio para los archivos de configuración de máquina virtual predeterminados. En la cadena de ruta de acceso, puede aparecer una barra diagonal inversa ( \\ ) inmediatamente antes del carácter nulo de terminación.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                               | Significado                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                                                 |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                                    | El *parámetro configurationPath* es **NULL.**<br/>                                                                                                |
| <dl> <dt>HRESULT \_ DESDE \_ WIN32(ARCHIVO DE ERROR \_ \_ NO \_ ENCONTRADO)</dt> <dt>0X80070002</dt> </dl> | El sistema no puede encontrar el directorio especificado por el *parámetro configurationPath.*<br/>                                                          |
| <dl> <dt>HRESULT \_ DESDE \_ WIN32(RUTA DE ACCESO DE ERROR \_ \_ NO \_ ENCONTRADA)</dt> <dt>0X80070003</dt> </dl> | El sistema no puede encontrar la ruta de acceso especificada por el *parámetro configurationPath.*<br/>                                                               |
| <dl> <dt>HRESULT \_ DESDE \_ WIN32(ERROR \_ NOMBRE NO \_ VÁLIDO)</dt> <dt>0x8007007b</dt> </dl>    | El *parámetro configurationPath* contiene un carácter no válido (uno de los siguientes: " \* ?<>/ \| ":").<br/>                                   |
| <dl> <dt>HRESULT \_ DESDE \_ WIN32(ERROR \_ BAD \_ PATHNAME)</dt> <dt>0x800700a1</dt> </dl>    | El *parámetro configurationPath* especifica una ruta de acceso vacía o relativa. Se requiere una ruta de acceso absoluta.<br/>                                          |
| <dl> <dt>HRESULT \_ DESDE \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)</dt> <dt>0x8007006f</dt> </dl> | La ruta de acceso especificada por el *parámetro configurationPath* es demasiado larga. La longitud de la ruta de acceso debe ser inferior a **MAX \_ PATH** (260) caracteres.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                                             |
| <dl> <dt>Máquina virtual \_ E \_ \_ VIRTUALIZACIÓN DE HARDWARE \_ DESHABILITADA</dt> <dt>0xA0040951</dt> </dl>     | El procesador no admite extensiones de virtualización acelerada de hardware (HAV).<br/>                                                          |



## <a name="remarks"></a>Comentarios

De forma predeterminada, este valor de propiedad se establece en el directorio siguiente: "%LocalAppData% \\ Microsoft Windows Virtual PC \\ \\ \\ Virtual Machines".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

