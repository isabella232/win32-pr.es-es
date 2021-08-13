---
title: Atributo system_handle
description: El atributo \ system_handle\ especifica un tipo de identificador definido por el sistema.
keywords:
- system_handle atributo MIDL
topic_type:
- apiref
api_name:
- system_handle
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 1cc89818db201f1aca84aa63c6aa49b6b7d9f80b7b6c5e211e724004606c653e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641271"
---
# <a name="system_handle-attribute"></a>Atributo system_handle

El system_handle especifica un tipo de identificador definido por el \[  \] sistema que representa el acceso a un objeto del sistema.

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*system-handle-type* 
</dt> <dd>

Especifica una de las opciones de tipo de identificador del sistema.

Las opciones válidas son:
* [sh_composition:](sh-composition.md) un identificador de superficie de DirectComposition
* [sh_event:](sh-event.md) un objeto de evento con nombre o sin nombre
* [sh_file:](sh-file.md) un archivo o un dispositivo de E/S
* [sh_job:](sh-job.md) un objeto de trabajo
* [sh_mutex:](sh-mutex.md) objeto de exclusión mutua con nombre o sin nombre
* [sh_pipe:](sh-pipe.md) objeto de canalización anónimo o con nombre
* [sh_process:](sh-process.md) un objeto de proceso
* [sh_reg_key:](sh-reg-key.md) una clave del Registro
* [sh_section:](sh-section.md) una sección de memoria compartida
* [sh_semaphore:](sh-semaphore.md) objeto semáforo con nombre o sin nombre
* [sh_socket:](sh-socket.md) un objeto de socket de WinSock
* [sh_thread:](sh-thread.md) un objeto de subproceso
* [sh_token:](sh-token.md) un objeto de token de acceso

</dd> <dt>

*optional-access-mask*
</dt> <dd>

Opcionalmente, solicita derechos de acceso específicos aplicados al identificador duplicado. De forma predeterminada, cuando esto no se especifica, el identificador se duplicará con el mismo acceso. 

Para especificar un nivel de acceso diferente, use derechos de acceso específicos del objeto correspondientes al objeto del sistema subyacente seleccionado.

Puede encontrar más información sobre cómo se propagan los derechos de acceso durante la duplicación en la [documentación de DuplicateHandle.](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

Los vínculos a listas de derechos de acceso para cada tipo de  objeto se pueden encontrar en la referencia *duplicateHandle,* así como en la página Ver también los encabezados de `sh_*` cada parámetro.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para usar este atributo, la `-target` marca debe establecerse en `NT100` (o superior) al ejecutar midl.exe.

Los identificadores del sistema son identificadores definidos por el sistema operativo para proporcionar acceso a un recurso del sistema. Se debe especificar el tipo específico del objeto detrás del identificador al declarar el atributo.

Para un identificador marcado como , el identificador se duplicará en el procedimiento remoto y seguirá siendo válido mientras `[in]` dure ese procedimiento. Cuando se devuelve desde el procedimiento remoto, se libera el identificador duplicado. Para mantener el acceso al objeto subyacente, la aplicación remota debe duplicar el identificador en su propio espacio de direcciones.

Por el contrario, para un identificador marcado como , cuando un procedimiento remoto devuelve un identificador de una llamada, el procedimiento remoto `[out]` perderá su propiedad. Para mantener el acceso al objeto subyacente, el procedimiento remoto debe duplicar el identificador y devolver el duplicado. A continuación, el identificador devuelto pasa a ser propiedad del autor de la llamada que asume la responsabilidad de cerrarlo cuando el acceso al objeto del sistema subyacente ya no es necesario.

Como se trata de un mecanismo para retransmitir el acceso a un objeto del sistema, este atributo solo es aplicable a las llamadas entre procedimientos en el mismo equipo.

Los parámetros de creación y acceso dados al objeto subyacente detrás del identificador del sistema en su creación determinarán si se pueden establecer correctamente en el contexto del procedimiento remoto.

Se puede pasar una matriz de con la sintaxis que se encuentra en la documentación `system_handle` [**size_is atributo.**](size-is.md)

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se usan varios de `system_handle` . Para obtener un ejemplo completo, vea [el ejemplo SystemHandlePassing.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)

```c
interface MyInterface : IUnknown                         
{         
    HRESULT Proc1([in, system_handle(sh_file)] HANDLE writeThisFile);

    HRESULT Proc2([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE readThisPipe);

    HRESULT Proc3([out, system_handle(sh_composition)] HANDLE* visual);

    HRESULT Proc4([in] DWORD cEvents, [out, system_handle(sh_event), size_is(cEvents)] HANDLE* pWatchAllTheseEvents);
}
```

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
|-|-|
| Cliente mínimo compatible | Windows 10 Actualización de aniversario (versión 1607, compilación 14393) |
| Servidor mínimo compatible | Windows Server 2016 (compilación 14393) |

## <a name="see-also"></a>Vea también

<dl> <dt>
<!--
[System Handle Passing sample code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)
</dt> <dt>
-->

[Modificador /target](./-target.md)
</dt> <dt>

[Enlace y identificadores](../Rpc/binding-and-handles.md)
</dt> <dt>

[Identificadores y objetos](../sysinfo/handles-and-objects.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[Descriptor de seguridad](../secauthz/security-descriptors.md)
</dt></dl>
