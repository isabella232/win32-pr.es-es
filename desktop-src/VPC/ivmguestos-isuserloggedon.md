---
title: Método IVMGuestOS IsUserLoggedOn (VPCCOMInterfaces. h)
description: Determina si la sesión solicitada está presente.
ms.assetid: 28035e30-023a-4ec2-88ef-43fe22f6d14e
keywords:
- Método IsUserLoggedOn Virtual PC
- Método IsUserLoggedOn Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, método IsUserLoggedOn
topic_type:
- apiref
api_name:
- IVMGuestOS.IsUserLoggedOn
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eeb0482d7d3ac45b67a863948526b57d6c6e412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695870"
---
# <a name="ivmguestosisuserloggedon-method"></a>IVMGuestOS:: IsUserLoggedOn (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina si la sesión solicitada está presente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsUserLoggedOn(
  [in]          long         inRailSession,
  [out, retval] VARIANT_BOOL *outSessionPresent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*inRailSession* \[ de\]
</dt> <dd>

Establezca en 0 para una sesión de raíl o 1 para una sesión de RDP.

</dd> <dt>

*outSessionPresent* \[ out, retval\]
</dt> <dd>

Establézcalo en **Variant \_ true** si la sesión está presente y **Variant \_ false** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                       | Descripción                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                             | La operación se realizó correctamente.<br/>                                   |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                               | El parámetro es **null**.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                            | El parámetro *outSessionPresent* no es válido o es **null**.<br/>  |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                       | Se produjo un error inesperado.<br/>                               |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl> | No hay suficiente memoria disponible para completar esta solicitud.<br/>  |
| <dl> <dt>**Máquina virtual \_ 0xA0040202 \_ agotó el tiempo de \_ espera**</dt> <dt></dt> </dl>                        | La operación no se completó de manera oportuna.<br/>              |
| <dl> <dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt> </dl>                  | La máquina virtual (VM) debe estar en ejecución para esta operación.<br/>    |
| <dl> <dt>**Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible**</dt> <dt>0xA0040505</dt> </dl>    | La característica componentes de integración no está instalada en esta máquina virtual.<br/> |
| <dl> <dt>**Máquina virtual \_ E/s de \_ VM en \_ pausa**</dt> <dt>0xA00400507</dt> </dl>                       | La máquina virtual está en pausa.<br/>                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

