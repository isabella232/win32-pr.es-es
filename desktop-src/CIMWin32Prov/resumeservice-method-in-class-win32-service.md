---
description: Intenta colocar el servicio al que se hace referencia en el estado de reanudación.
ms.assetid: 3b4228bf-9ff5-44ab-bfe2-f7dd8fb62007
ms.tgt_platform: multiple
title: Método ResumeService de la clase Win32_Service (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ed4141b02d6e08bd4b106d2c1f72ce3fe0620fc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907501"
---
# <a name="resumeservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Método ResumeService de la clase Win32_Service (proveedores WMI de CIMWin32)

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ResumeService** intenta colocar el servicio al que se hace referencia en el estado de reanudación.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 ResumeService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Se aceptó la solicitud.

</dd> <dt>

**1**
</dt> <dd>

No se admite la solicitud.

</dd> <dt>

**2**
</dt> <dd>

El usuario no tenía el acceso necesario.

</dd> <dt>

**3**
</dt> <dd>

No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.

</dd> <dt>

**4**
</dt> <dd>

El código de control solicitado no es válido o no es aceptable para el servicio.

</dd> <dt>

**5**
</dt> <dd>

El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.

</dd> <dt>

**6**
</dt> <dd>

El servicio no se ha iniciado.

</dd> <dt>

**7**
</dt> <dd>

El servicio no respondió a tiempo a la solicitud de inicio.

</dd> <dt>

**8**
</dt> <dd>

Error desconocido al iniciar el servicio.

</dd> <dt>

**9**
</dt> <dd>

No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.

</dd> <dt>

**10**
</dt> <dd>

El servicio ya se está ejecutando.

</dd> <dt>

**11**
</dt> <dd>

La base de datos para agregar un nuevo servicio está bloqueada.

</dd> <dt>

**12**
</dt> <dd>

Una dependencia de la que depende este servicio se ha quitado del sistema.

</dd> <dt>

**13**
</dt> <dd>

El servicio no pudo encontrar el servicio necesario de un servicio dependiente.

</dd> <dt>

**14**
</dt> <dd>

El servicio se ha deshabilitado del sistema.

</dd> <dt>

**15**
</dt> <dd>

El servicio no tiene la autenticación correcta para ejecutarse en el sistema.

</dd> <dt>

**16**
</dt> <dd>

Este servicio se está quitando del sistema.

</dd> <dt>

**17**
</dt> <dd>

El servicio no tiene ningún subproceso de ejecución.

</dd> <dt>

**18**
</dt> <dd>

El servicio tiene dependencias circulares al iniciarse.

</dd> <dt>

**19**
</dt> <dd>

Se está ejecutando un servicio con el mismo nombre.

</dd> <dt>

**20**
</dt> <dd>

El nombre del servicio tiene caracteres no válidos.

</dd> <dt>

**21**
</dt> <dd>

Se han pasado parámetros no válidos al servicio.

</dd> <dt>

**22**
</dt> <dd>

La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.

</dd> <dt>

**23**
</dt> <dd>

El servicio existe en la base de datos de servicios disponibles del sistema.

</dd> <dt>

**24**
</dt> <dd>

El servicio se encuentra en pausa actualmente en el sistema.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Aunque puede parecer que no hay ninguna diferencia práctica entre un servicio detenido y un servicio que está en pausa, los dos Estados aparecen de manera diferente en el SCM. Un servicio detenido es un servicio que no se está ejecutando y debe recorrer todo el procedimiento de inicio del servicio. Un servicio en pausa, sin embargo, todavía se está ejecutando pero se ha suspendido su funcionamiento. Por este motivo, un servicio en pausa no necesita recorrer todo el procedimiento de inicio del servicio, pero necesita un procedimiento diferente para reanudar el funcionamiento.

Debe usar el método adecuado para iniciar un servicio que se ha detenido o para reanudar un servicio que se ha pausado. Los métodos de [**\_ servicio de Win32**](win32-service.md) [**StartService**](startservice-method-in-class-win32-service.md) y **ResumeService** deben usarse en las siguientes situaciones:

-   Si un servicio está detenido actualmente, debe utilizar el método [**StartService**](startservice-method-in-class-win32-service.md) para reiniciarlo; **ResumeService** no puede iniciar un servicio que está detenido actualmente.
-   Si un servicio está en pausa, debe utilizar **ResumeService**. Si usa el método [**StartService**](startservice-method-in-class-win32-service.md) en un servicio en pausa, recibirá el mensaje "el servicio ya se está ejecutando". Sin embargo, el servicio permanece en pausa hasta que se le envíe el código de control de servicio de reanudación.

## <a name="examples"></a>Ejemplos

En el ejemplo de [reanudación de los servicios de inicio automático que se encuentran en pausa](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) de VBScript se reinician los servicios de inicio automático que se han pausado.

En el siguiente ejemplo de código de VBScript se describe cómo reanudar un servicio en pausa desde instancias del [**\_ servicio de Win32**](win32-service.md).

> [!Note]  
> El servicio debe admitir la pausa y ya se está ejecutando.

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.ResumeService()
  if RetVal = 0 then 
   WScript.Echo "Service resumed"   
  else
   if RetVal = 1 then 
    WScript.Echo "Pause not supported" 
   else WScript.Echo "An error occurred:" & RetVal
   End If
  End If
 else
  WScript.Echo "Service does not support pause"
 end if
next
```



El siguiente ejemplo de código Perl describe cómo reanudar un servicio en pausa desde instancias [**del \_ servicio de Win32**](win32-service.md).

> [!Note]  
> El servicio debe admitir la pausa y ya se está ejecutando.

 


```Perl
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $Service (in $ServiceSet)
 {
  my $SupportsPause = $Service->{AcceptPause};
  if ($SupportsPause)
  {
   my $RetVal = $Service->ResumeService();
   if ($RetVal == 0)
   {
    print "\nService resumed\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print STDERR "\nPause not supported\n";
    }
    else
    {
     print STDERR "\nAn error occurred: ", $RetVal, "\n";
    }
   }
  }
  else
  {
   print "\nService does not support pause\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Servicio Win32**](win32-service.md)
</dt> <dt>

[Tareas WMI: servicios](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

