---
title: Método IVMGuestOS GetParameter (VPCCOMInterfaces.h)
description: Recupera un parámetro con nombre dentro del sistema operativo invitado.
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- Método GetParameter de Virtual PC
- Método GetParameter Virtual PC , interfaz IVMGuestOS
- IVMGuestOS interface Virtual PC , Método GetParameter
topic_type:
- apiref
api_name:
- IVMGuestOS.GetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 955b70986640fab8cefe9f02b28b02015397c964f1b10fc26057533fc79a3809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753567"
---
# <a name="ivmguestosgetparameter-method"></a>IVMGuestOS::GetParameter (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera un parámetro con nombre dentro del sistema operativo invitado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*inParameterName* \[ En\]
</dt> <dd>

Nombre del parámetro. Debe tener entre 1 y 255 caracteres de longitud y no puede contener un carácter de barra diagonal inversa ( \\ ).

</dd> <dt>

*outParameterValue* \[ out, retval\]
</dt> <dd>

Valor del parámetro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                    | Descripción                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                                     |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>                         | Un parámetro no es válido o no se especifica.<br/>                        |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                            | El parámetro es **NULL.**<br/>                                        |
| <dl> <dt>**Máquina virtual \_ E \_ TIEMPO DE ESPERA \_ 0XA0040202**</dt> <dt></dt> </dl>                     | La operación no se ha completado a tiempo.<br/>                |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>               | La máquina virtual no se está ejecutando.<br/>                               |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ PAUSED**</dt> <dt>0xA00400507</dt> </dl>                    | La máquina virtual está en pausa.<br/>                                    |
| <dl> <dt>**Máquina virtual \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0XA0040505</dt> </dl> | Los componentes de integración no están instalados en esta máquina virtual.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                                 |



 

## <a name="remarks"></a>Comentarios

La máquina virtual debe estar en ejecución y los componentes de integración deben instalarse cuando se invoca este método. Este método solo se admite para Windows operativos invitados basados en el usuario.

Con los componentes de integración instalados, la siguiente clave se agrega automáticamente al registro del sistema operativo invitado:

**HKEY \_ LOCAL MACHINE SOFTWARE Parámetros \_ \\ \\ invitados de la máquina virtual \\ \\ \\ de Microsoft**

Cuando se inicia el sistema operativo invitado, se rellenan los siguientes valores de cadena del Registro en la **clave** Parameters:

-   **HostName**
-   **PhysicalHostName**
-   **PhysicalHostNameFullyQualified**
-   **VirtualMachineName**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS se define como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

