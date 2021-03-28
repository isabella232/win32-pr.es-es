---
description: Cierra el subproceso de resolución de nombres de usuario.
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: Método DiskQuotaControl. ShutdownNameResolution (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.ShutdownNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0db952a502210e509abeb527b2006eab087434e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082072"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a>DiskQuotaControl. ShutdownNameResolution, método

Cierra el subproceso de resolución de nombres de usuario.

## <a name="syntax"></a>Sintaxis


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La resolución de nombres del identificador de seguridad (SID) traduce el SID a los nombres de usuario en un subproceso en segundo plano. Este subproceso se cierra automáticamente cuando se destruye el objeto de control de cuota asociado. Sin embargo, hay algunos casos en los que el subproceso ya no se necesita, pero el objeto todavía no está listo para ser destruido. Un ejemplo típico es cuando no se realiza ningún otro procesamiento, pero los clientes siguen conservando las referencias al objeto. El método **ShutdownNameResolution** permite terminar el subproceso de resolución y liberar los recursos asociados sin destruir el objeto de control de cuota.

> [!Note]  
> Al cerrar el subproceso de resolución, se detiene inmediatamente la resolución de nombres asincrónica. Si posteriormente se realizan llamadas a métodos como [**adduser**](diskquotacontrol-adduser.md) o [**FindUser**](diskquotacontrol-finduser.md), el objeto de cuota podría volver a crear el subproceso de resolución.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




