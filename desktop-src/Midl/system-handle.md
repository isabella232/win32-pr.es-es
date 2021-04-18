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
# <a name="system_handle-attribute"></a><span data-ttu-id="7c338-104">Atributo system_handle</span><span class="sxs-lookup"><span data-stu-id="7c338-104">system_handle attribute</span></span>

<span data-ttu-id="7c338-105">El \[  \] atributo system_handle especifica un tipo de identificador definido por el sistema que representa el acceso a un objeto del sistema.</span><span class="sxs-lookup"><span data-stu-id="7c338-105">The \[**system_handle**\] attribute specifies a system-defined handle type that represents access to a system object.</span></span>

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a><span data-ttu-id="7c338-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c338-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c338-107">*tipo de controlador del sistema*</span><span class="sxs-lookup"><span data-stu-id="7c338-107">*system-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7c338-108">Especifica una de las opciones de tipo de identificador del sistema.</span><span class="sxs-lookup"><span data-stu-id="7c338-108">Specifies one of the system handle type options.</span></span>

<span data-ttu-id="7c338-109">Las opciones válidas son:</span><span class="sxs-lookup"><span data-stu-id="7c338-109">The valid options are:</span></span>
* <span data-ttu-id="7c338-110">[sh_composition](sh-composition.md) : controlador de la superficie DirectComposition</span><span class="sxs-lookup"><span data-stu-id="7c338-110">[sh_composition](sh-composition.md) - A DirectComposition surface handle</span></span>
* <span data-ttu-id="7c338-111">[sh_event](sh-event.md) : objeto de evento con nombre o sin nombre</span><span class="sxs-lookup"><span data-stu-id="7c338-111">[sh_event](sh-event.md) - A named or unnamed event object</span></span>
* <span data-ttu-id="7c338-112">[sh_file](sh-file.md) : un archivo o un dispositivo de e/s</span><span class="sxs-lookup"><span data-stu-id="7c338-112">[sh_file](sh-file.md) - A file or I/O device</span></span>
* <span data-ttu-id="7c338-113">[sh_job](sh-job.md) : un objeto de trabajo</span><span class="sxs-lookup"><span data-stu-id="7c338-113">[sh_job](sh-job.md) - A job object</span></span>
* <span data-ttu-id="7c338-114">[sh_mutex](sh-mutex.md) : objeto mutex con nombre o sin nombre</span><span class="sxs-lookup"><span data-stu-id="7c338-114">[sh_mutex](sh-mutex.md) - A named or unnamed mutex object</span></span>
* <span data-ttu-id="7c338-115">[sh_pipe](sh-pipe.md) : un objeto de canalización anónimo o con nombre</span><span class="sxs-lookup"><span data-stu-id="7c338-115">[sh_pipe](sh-pipe.md) - An anonymous or named pipe object</span></span>
* <span data-ttu-id="7c338-116">[sh_process](sh-process.md) : objeto de proceso</span><span class="sxs-lookup"><span data-stu-id="7c338-116">[sh_process](sh-process.md) - A process object</span></span>
* <span data-ttu-id="7c338-117">[sh_reg_key](sh-reg-key.md) -una clave del registro</span><span class="sxs-lookup"><span data-stu-id="7c338-117">[sh_reg_key](sh-reg-key.md) - A registry key</span></span>
* <span data-ttu-id="7c338-118">[sh_section](sh-section.md) : sección de memoria compartida</span><span class="sxs-lookup"><span data-stu-id="7c338-118">[sh_section](sh-section.md) - A shared memory section</span></span>
* <span data-ttu-id="7c338-119">[sh_semaphore](sh-semaphore.md) : un objeto de semáforo con nombre o sin nombre</span><span class="sxs-lookup"><span data-stu-id="7c338-119">[sh_semaphore](sh-semaphore.md) - A named or unnamed semaphore object</span></span>
* <span data-ttu-id="7c338-120">[sh_socket](sh-socket.md) : un objeto socket de Winsock</span><span class="sxs-lookup"><span data-stu-id="7c338-120">[sh_socket](sh-socket.md) - A WinSock socket object</span></span>
* <span data-ttu-id="7c338-121">[sh_thread](sh-thread.md) : objeto Thread</span><span class="sxs-lookup"><span data-stu-id="7c338-121">[sh_thread](sh-thread.md) - A thread object</span></span>
* <span data-ttu-id="7c338-122">[sh_token](sh-token.md) : un objeto de token de acceso</span><span class="sxs-lookup"><span data-stu-id="7c338-122">[sh_token](sh-token.md) - An access token object</span></span>

</dd> <dt>

<span data-ttu-id="7c338-123">*opcional: máscara de acceso*</span><span class="sxs-lookup"><span data-stu-id="7c338-123">*optional-access-mask*</span></span>
</dt> <dd>

<span data-ttu-id="7c338-124">Opcionalmente, solicita derechos de acceso específicos aplicados al identificador duplicado.</span><span class="sxs-lookup"><span data-stu-id="7c338-124">Optionally requests specific access rights applied to the duplicated handle.</span></span> <span data-ttu-id="7c338-125">De forma predeterminada, cuando no se especifica, el identificador se duplicará con el mismo acceso.</span><span class="sxs-lookup"><span data-stu-id="7c338-125">By default when this is unspecified, the handle will be duplicated with the same access.</span></span> 

<span data-ttu-id="7c338-126">Para especificar un nivel de acceso diferente, utilice los derechos de acceso específicos del objeto que se corresponden con el objeto del sistema subyacente seleccionado.</span><span class="sxs-lookup"><span data-stu-id="7c338-126">To specify a different level of access, use object specific access rights corresponding to the underlying system object selected.</span></span>

<span data-ttu-id="7c338-127">Puede encontrar más información sobre cómo se propagan los derechos de acceso durante la duplicación en la documentación de [DuplicateHandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="7c338-127">More information on how access rights are propagated during duplication can be found on the [DuplicateHandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) documentation.</span></span>

<span data-ttu-id="7c338-128">Los vínculos a las listas de derechos de acceso para cada tipo de objeto se pueden encontrar en la referencia de *DuplicateHandle* , así como en los encabezados **vea también** de cada `sh_*` Página de parámetros.</span><span class="sxs-lookup"><span data-stu-id="7c338-128">Links to lists of access rights for each type of object can be found in the *DuplicateHandle* reference as well as in the **See also** headings of each `sh_*` parameter page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c338-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c338-129">Remarks</span></span>

<span data-ttu-id="7c338-130">Para usar este atributo, la `-target` marca debe establecerse en `NT100` (o superior) al ejecutarse midl.exe.</span><span class="sxs-lookup"><span data-stu-id="7c338-130">In order to use this attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

<span data-ttu-id="7c338-131">Los identificadores del sistema son identificadores definidos por el sistema operativo para proporcionar acceso a un recurso del sistema.</span><span class="sxs-lookup"><span data-stu-id="7c338-131">System handles are handles that are defined by the operating system to provide access to a system resource.</span></span> <span data-ttu-id="7c338-132">El tipo específico del objeto situado detrás del identificador debe especificarse al declarar el atributo.</span><span class="sxs-lookup"><span data-stu-id="7c338-132">The specific type of the object behind the handle must be specified when declaring the attribute.</span></span>

<span data-ttu-id="7c338-133">En el caso de un identificador marcado `[in]` , el identificador se duplicará en el procedimiento remoto y seguirá siendo válido mientras dure dicho procedimiento.</span><span class="sxs-lookup"><span data-stu-id="7c338-133">For a handle marked `[in]`, the handle will be duplicated into the remote procedure and remains valid for the duration of that procedure.</span></span> <span data-ttu-id="7c338-134">Al volver del procedimiento remoto, se libera el identificador duplicado.</span><span class="sxs-lookup"><span data-stu-id="7c338-134">On return from the remote procedure, the duplicated handle is freed.</span></span> <span data-ttu-id="7c338-135">Para mantener el acceso al objeto subyacente, la aplicación remota debe duplicar el identificador en su propio espacio de direcciones.</span><span class="sxs-lookup"><span data-stu-id="7c338-135">To maintain access to the underlying object, the remote application must duplicate the handle into its own address space.</span></span>

<span data-ttu-id="7c338-136">Por el contrario, para un identificador marcado `[out]` , cuando un procedimiento remoto devuelve un identificador de una llamada, el procedimiento remoto perderá su propiedad.</span><span class="sxs-lookup"><span data-stu-id="7c338-136">By contrast, for a handle marked `[out]`, when a remote procedure returns a handle from a call, the remote procedure will lose ownership of it.</span></span> <span data-ttu-id="7c338-137">Para mantener el acceso al objeto subyacente, el procedimiento remoto debe duplicar el identificador y devolver el duplicado.</span><span class="sxs-lookup"><span data-stu-id="7c338-137">To maintain access to the underlying object, the remote procedure should duplicate the handle and return the duplicate.</span></span> <span data-ttu-id="7c338-138">El identificador devuelto se convierte entonces en propiedad del llamador que asume la responsabilidad de cerrarlo cuando ya no es necesario el acceso al objeto del sistema subyacente.</span><span class="sxs-lookup"><span data-stu-id="7c338-138">The returned handle then becomes owned by the caller who assumes a responsibility to close it when access to the underlying system object is no longer necessary.</span></span>

<span data-ttu-id="7c338-139">Dado que se trata de un mecanismo para retransmitir el acceso a un objeto del sistema, este atributo solo se aplica a las llamadas entre procedimientos en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="7c338-139">As this is a mechanism for relaying access to a system object, this attribute is only applicable to calls between procedures on the same machine.</span></span>

<span data-ttu-id="7c338-140">Los parámetros de creación y acceso proporcionados al objeto subyacente detrás del identificador del sistema en su creación determinarán si se pueden calcular correctamente las referencias al contexto del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="7c338-140">The creation and access parameters given to the underlying object behind the system handle on its creation will dictate whether it can be successfully marshalled to the remote procedure context.</span></span>

<span data-ttu-id="7c338-141">Una matriz de `system_handle` se puede pasar dentro o fuera de con la sintaxis que se encuentra en la documentación del [**atributo de size_is**](size-is.md) .</span><span class="sxs-lookup"><span data-stu-id="7c338-141">An array of `system_handle` can be passed either in or out with the syntax found in the [**size_is attribute**](size-is.md) documentation.</span></span>

## <a name="examples"></a><span data-ttu-id="7c338-142">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7c338-142">Examples</span></span>

<span data-ttu-id="7c338-143">En los siguientes ejemplos se usan varios `system_handle` .</span><span class="sxs-lookup"><span data-stu-id="7c338-143">The following examples several uses of `system_handle`.</span></span> <span data-ttu-id="7c338-144">Para obtener un ejemplo completo, vea el ejemplo [SystemHandlePassing](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) .</span><span class="sxs-lookup"><span data-stu-id="7c338-144">For a complete sample, see the [SystemHandlePassing](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) sample.</span></span>

```c
interface MyInterface : IUnknown                         
{         
    HRESULT Proc1([in, system_handle(sh_file)] HANDLE writeThisFile);

    HRESULT Proc2([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE readThisPipe);

    HRESULT Proc3([out, system_handle(sh_composition)] HANDLE* visual);

    HRESULT Proc4([in] DWORD cEvents, [out, system_handle(sh_event), size_is(cEvents)] HANDLE* pWatchAllTheseEvents);
}
```

## <a name="requirements"></a><span data-ttu-id="7c338-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c338-145">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="7c338-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c338-146">Minimum supported client</span></span> | <span data-ttu-id="7c338-147">Actualización de aniversario de Windows 10 (versión 1607, compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="7c338-147">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="7c338-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c338-148">Minimum supported server</span></span> | <span data-ttu-id="7c338-149">Windows Server 2016 (compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="7c338-149">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="7c338-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c338-150">See also</span></span>

<dl> <dt>
<!--
[System Handle Passing sample code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)
</dt> <dt>
-->

[<span data-ttu-id="7c338-151">Modificador /target</span><span class="sxs-lookup"><span data-stu-id="7c338-151">/target switch</span></span>](./-target.md)
</dt> <dt>

[<span data-ttu-id="7c338-152">Enlace y controladores</span><span class="sxs-lookup"><span data-stu-id="7c338-152">Binding and Handles</span></span>](../Rpc/binding-and-handles.md)
</dt> <dt>

[<span data-ttu-id="7c338-153">Identificadores y objetos</span><span class="sxs-lookup"><span data-stu-id="7c338-153">Handles and Objects</span></span>](../sysinfo/handles-and-objects.md)
</dt> <dt>

[<span data-ttu-id="7c338-154">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="7c338-154">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7c338-155">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="7c338-155">**DuplicateHandle**</span></span>](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[<span data-ttu-id="7c338-156">Descriptor de seguridad</span><span class="sxs-lookup"><span data-stu-id="7c338-156">Security Descriptors</span></span>](../secauthz/security-descriptors.md)
</dt></dl>
