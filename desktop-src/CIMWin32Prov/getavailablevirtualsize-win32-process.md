---
description: Recupera el tamaño actual, en bytes, del espacio de direcciones virtuales libre disponible para el proceso.
ms.assetid: 13b3b347-5db1-484f-bd1d-3a604eb6bc5b
ms.tgt_platform: multiple
title: Método GetAvailableVirtualSize de la clase Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetAvailableVirtualSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ee6e798b8df32822de481f3af1dc6b21a81d1024
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659482"
---
# <a name="getavailablevirtualsize-method-of-the-win32_process-class"></a>Método GetAvailableVirtualSize de la \_ clase Process de Win32

Recupera el tamaño actual, en bytes, del espacio de direcciones virtuales libre disponible para el proceso.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetAvailableVirtualSize(
  [out] uint64 AvailableVirtualSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AvailableVirtualSize* \[ enuncia\]
</dt> <dd>

El parámetro *AvailableVirtualSize* devuelve el espacio de direcciones virtuales disponible para este proceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero (0) para indicar que la operación se ha realizado correctamente. Cualquier otro número indica que hubo un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Completado correctamente.**
</dt> <dd>

0

La operación se ha completado correctamente.

</dd> <dt>

**Acceso denegado**
</dt> <dd>

2

El usuario no tiene acceso a la información solicitada.

</dd> <dt>

**Privilegio insuficiente**
</dt> <dd>

3

El usuario no tiene privilegios suficientes.

</dd> <dt>

**Error desconocido**
</dt> <dd>

8

Error desconocido.

</dd> <dt>

**No se encuentra la ruta de acceso**
</dt> <dd>

9

La ruta especificada no existe.

</dd> <dt>

**parámetro no válido**
</dt> <dd>

21

El parámetro especificado no es válido.

</dd> <dt>

**Otros**
</dt> <dd>

22 4294967295

Para valores distintos de los enumerados, consulte la documentación de [códigos de error del sistema](/windows/desktop/Debug/system-error-codes) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                       |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Proceso Win32**](win32-process.md)
</dt> </dl>

 

