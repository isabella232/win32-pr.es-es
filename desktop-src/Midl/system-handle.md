---
title: Atributo system_handle
description: El atributo \ system_handle \ especifica un tipo de identificador definido por el sistema.
keywords:
- system_handle el atributo MIDL
topic_type:
- apiref
api_name:
- system_handle
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: f414654cdbd2eb07837455174f6142005f56a4b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105721346"
---
# <a name="system_handle-attribute"></a>Atributo system_handle

El \[  \] atributo system_handle especifica un tipo de identificador definido por el sistema que representa el acceso a un objeto del sistema.

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo de controlador del sistema* 
</dt> <dd>

Especifica una de las opciones de tipo de identificador del sistema.

Las opciones válidas son:
* [sh_composition](sh-composition.md) : controlador de la superficie DirectComposition
* [sh_event](sh-event.md) : objeto de evento con nombre o sin nombre
* [sh_file](sh-file.md) : un archivo o un dispositivo de e/s
* [sh_job](sh-job.md) : un objeto de trabajo
* [sh_mutex](sh-mutex.md) : objeto mutex con nombre o sin nombre
* [sh_pipe](sh-pipe.md) : un objeto de canalización anónimo o con nombre
* [sh_process](sh-process.md) : objeto de proceso
* [sh_reg_key](sh-reg-key.md) -una clave del registro
* [sh_section](sh-section.md) : sección de memoria compartida
* [sh_semaphore](sh-semaphore.md) : un objeto de semáforo con nombre o sin nombre
* [sh_socket](sh-socket.md) : un objeto socket de Winsock
* [sh_thread](sh-thread.md) : objeto Thread
* [sh_token](sh-token.md) : un objeto de token de acceso

</dd> <dt>

*opcional: máscara de acceso*
</dt> <dd>

Opcionalmente, solicita derechos de acceso específicos aplicados al identificador duplicado. De forma predeterminada, cuando no se especifica, el identificador se duplicará con el mismo acceso. 

Para especificar un nivel de acceso diferente, utilice los derechos de acceso específicos del objeto que se corresponden con el objeto del sistema subyacente seleccionado.

Puede encontrar más información sobre cómo se propagan los derechos de acceso durante la duplicación en la documentación de [DuplicateHandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

Los vínculos a las listas de derechos de acceso para cada tipo de objeto se pueden encontrar en la referencia de *DuplicateHandle* , así como en los encabezados **vea también** de cada `sh_*` Página de parámetros.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para usar este atributo, la `-target` marca debe establecerse en `NT100` (o superior) al ejecutarse midl.exe.

Los identificadores del sistema son identificadores definidos por el sistema operativo para proporcionar acceso a un recurso del sistema. El tipo específico del objeto situado detrás del identificador debe especificarse al declarar el atributo.

En el caso de un identificador marcado `[in]` , el identificador se duplicará en el procedimiento remoto y seguirá siendo válido mientras dure dicho procedimiento. Al volver del procedimiento remoto, se libera el identificador duplicado. Para mantener el acceso al objeto subyacente, la aplicación remota debe duplicar el identificador en su propio espacio de direcciones.

Por el contrario, para un identificador marcado `[out]` , cuando un procedimiento remoto devuelve un identificador de una llamada, el procedimiento remoto perderá su propiedad. Para mantener el acceso al objeto subyacente, el procedimiento remoto debe duplicar el identificador y devolver el duplicado. El identificador devuelto se convierte entonces en propiedad del llamador que asume la responsabilidad de cerrarlo cuando ya no es necesario el acceso al objeto del sistema subyacente.

Dado que se trata de un mecanismo para retransmitir el acceso a un objeto del sistema, este atributo solo se aplica a las llamadas entre procedimientos en el mismo equipo.

Los parámetros de creación y acceso proporcionados al objeto subyacente detrás del identificador del sistema en su creación determinarán si se pueden calcular correctamente las referencias al contexto del procedimiento remoto.

Una matriz de `system_handle` se puede pasar dentro o fuera de con la sintaxis que se encuentra en la documentación del [**atributo de size_is**](size-is.md) .

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos se usan varios `system_handle` . Para obtener un ejemplo completo, vea el ejemplo [SystemHandlePassing](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) .

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
| Cliente mínimo compatible | Actualización de aniversario de Windows 10 (versión 1607, compilación 14393) |
| Servidor mínimo compatible | Windows Server 2016 (compilación 14393) |

## <a name="see-also"></a>Vea también

<dl> <dt>
<!--
[System Handle Passing sample code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)
</dt> <dt>
-->

[Modificador /target](./-target.md)
</dt> <dt>

[Enlace y controladores](../Rpc/binding-and-handles.md)
</dt> <dt>

[Identificadores y objetos](../sysinfo/handles-and-objects.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[Descriptor de seguridad](../secauthz/security-descriptors.md)
</dt></dl>
