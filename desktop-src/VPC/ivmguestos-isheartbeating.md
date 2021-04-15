---
title: Propiedad IVMGuestOS IsHeartbeating (VPCCOMInterfaces. h)
description: Determina si la máquina virtual tiene un latido.
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- Propiedad IsHeartbeating Virtual PC
- Propiedad IsHeartbeating Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad IsHeartbeating
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHeartbeating
- IVMGuestOS.get_IsHeartbeating
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faad446749cbf3cdb75d6e8fa7469022cc004ea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696043"
---
# <a name="ivmguestosisheartbeating-property"></a>IVMGuestOS:: IsHeartbeating (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina si la máquina virtual tiene un latido.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a>Valor de propiedad

**Variante \_ TRUE** si se detecta un latido, **Variant \_ false** en caso contrario.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                              | Significado                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                 | La operación se realizó correctamente.<br/>                                                                                                                         |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                   | El parámetro es **null**.<br/>                                                                                                                            |
| <dl> <dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt> </dl>           | La configuración es desconocida.<br/>                                                                                                                         |
| <dl> <dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt> </dl>      | La máquina virtual debe estar en ejecución para esta operación.<br/>                                                                                               |
| <dl> <dt>Máquina virtual \_ E/s \_ \_ no \_ DISP</dt> <dt>0xA0040504</dt> </dl> | La máquina virtual no se ha iniciado completamente, la característica componentes de integración no está instalada o la versión instalada no es compatible con esta característica.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>           | Se produjo un error inesperado.<br/>                                                                                                                     |



## <a name="remarks"></a>Observaciones

Cuando se instalan los componentes de integración en el sistema operativo invitado, se envía un "tick" o latido normal desde la sesión de máquina virtual a Windows Virtual PC. Si el sistema operativo invitado está muy cargado, es posible que el equipo virtual reciba menos latidos de lo esperado. Si no se detecta ningún latido, es posible que el sistema operativo invitado no responda o se bloquee.

De forma predeterminada, una máquina virtual produce diez TICs de latido por minuto. Si no se detectan TICs de latidos durante un minuto completo, Windows Virtual PC intentará reiniciar la sesión de máquina virtual una vez cada diez segundos durante un máximo de dos minutos. Este comportamiento se controla mediante los siguientes valores de clave en el archivo de configuración de la sesión de máquina virtual.



| Clave de configuración                                            | Valor predeterminado       | Descripción                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| integración/Microsoft/latido/hora<br/>              | 60<br/> | La longitud del bloque de tiempo usado para generar TICs de latido, en segundos.<br/>                                             |
| integración/Microsoft/latido/tasa<br/>              | 10<br/> | Número de pasos generados en cada bloque de tiempo de latido.<br/>                                                                  |
| integración/Microsoft/latido/intervalo de errores \_<br/> | 10<br/> | El número de segundos entre los intentos de reinicio, una vez que no se reciben TICs de latido dentro de un bloque de tiempo de latido específico.<br/> |
| integración/Microsoft/latido/intentos de error \_<br/> | 12<br/> | El número de intentos de reinicio realizados.<br/>                                                                                         |



 

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

 

