---
description: Intenta colocar el servicio al que se hace referencia en estado en pausa.
ms.assetid: 57b8ccdd-056a-4bec-a0f8-ecebcf18039e
ms.tgt_platform: multiple
title: Método PauseService de la Win32_BaseService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.PauseService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4828b81af5d6d543aaf16a34a08350f09078d623
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062690"
---
# <a name="pauseservice-method-of-the-win32_baseservice-class"></a>Método PauseService de la clase BaseService win32 \_

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** intenta colocar el servicio al que se hace referencia en estado en pausa.

En este tema se Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 PauseService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.

<dl> <dt>

**Success**
</dt> <dd>

0

Se aceptó la solicitud.

</dd> <dt>

**No compatible**
</dt> <dd>

1

No se admite la solicitud.

</dd> <dt>

**Acceso denegado**
</dt> <dd>

2

El usuario no tenía el acceso necesario.

</dd> <dt>

**Servicios dependientes en ejecución**
</dt> <dd>

3

No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.

</dd> <dt>

**Control de servicio no válido**
</dt> <dd>

4

El código de control solicitado no es válido o no es aceptable para el servicio.

</dd> <dt>

**El servicio no puede aceptar el control**
</dt> <dd>

5

El código de control solicitado no se puede enviar al servicio porque el estado del servicio (propiedad [**Estado de \_ BaseService de Win32)**](win32-baseservice.md)es igual a 0, 1 o 2.[](win32-baseservice.md)

</dd> <dt>

**Servicio no activo**
</dt> <dd>

6

El servicio no se ha iniciado.

</dd> <dt>

**Tiempo de espera de solicitud de servicio**
</dt> <dd>

7

El servicio no respondió a tiempo a la solicitud de inicio.

</dd> <dt>

**Error desconocido**
</dt> <dd>

8

Proceso interactivo.

</dd> <dt>

**Ruta de acceso no encontrada**
</dt> <dd>

9

No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.

</dd> <dt>

**Servicio ya en ejecución**
</dt> <dd>

10

El servicio ya se está ejecutando.

</dd> <dt>

**Base de datos de servicio bloqueada**
</dt> <dd>

11

La base de datos para agregar un nuevo servicio está bloqueada.

</dd> <dt>

**Dependencia de servicio eliminada**
</dt> <dd>

12

Una dependencia en la que se basaba este servicio se ha quitado del sistema.

</dd> <dt>

**Error de dependencia de servicio**
</dt> <dd>

13

El servicio no pudo encontrar el servicio necesario de un servicio dependiente.

</dd> <dt>

**Servicio deshabilitado**
</dt> <dd>

14

El servicio se ha deshabilitado del sistema.

</dd> <dt>

**Error de inicio de sesión de servicio**
</dt> <dd>

15

El servicio no tiene la autenticación correcta para ejecutarse en el sistema.

</dd> <dt>

**Servicio marcado para eliminación**
</dt> <dd>

16

Este servicio se está quitando del sistema.

</dd> <dt>

**Servicio sin subproceso**
</dt> <dd>

17

No hay ningún subproceso de ejecución para el servicio.

</dd> <dt>

**Dependencia circular de estado**
</dt> <dd>

18

Hay dependencias circulares al iniciarse el servicio.

</dd> <dt>

**Nombre duplicado de estado**
</dt> <dd>

19

Hay un servicio que se ejecuta con el mismo nombre.

</dd> <dt>

**Nombre de estado no válido**
</dt> <dd>

20

Hay caracteres no válidos en el nombre del servicio.

</dd> <dt>

**Parámetro Status Invalid**
</dt> <dd>

21

Se han pasado parámetros no válidos al servicio.

</dd> <dt>

**Cuenta de servicio de estado no válida**
</dt> <dd>

22

La cuenta en la que se va a ejecutar este servicio no es válida o carece de los permisos para ejecutar el servicio.

</dd> <dt>

**El servicio de estado existe**
</dt> <dd>

23

El servicio existe en la base de datos de servicios disponibles del sistema.

</dd> <dt>

**Servicio ya en pausa**
</dt> <dd>

24

El servicio se encuentra en pausa actualmente en el sistema.

</dd> <dt>

**Otros**
</dt> <dd>

25 4294967295

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**BaseService de Win32 \_**](win32-baseservice.md)
</dt> </dl>

 

