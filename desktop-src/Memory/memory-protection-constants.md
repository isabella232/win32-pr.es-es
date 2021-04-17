---
Description: A continuación se muestran las opciones de protección de memoria; debe especificar uno de los siguientes valores al asignar o proteger una página en la memoria. No se pueden asignar atributos de protección a una parte de una página; solo se pueden asignar a una página completa.
ms.assetid: 09839db7-2118-4a7d-a707-a08c92bd600c
title: Constantes de protección de memoria (Winnt. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 641fab68024d9db96f50327f7c78d51f3f9bca01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670554"
---
# <a name="memory-protection-constants"></a>Constantes de protección de memoria

A continuación se muestran las opciones de protección de memoria; debe especificar uno de los siguientes valores al asignar o proteger una página en la memoria. No se pueden asignar atributos de protección a una parte de una página; solo se pueden asignar a una página completa.

## <a name="example"></a>Ejemplo

```cpp
STDMETHODIMP CExtBuffer::FInit
    (
    ULONG cItemMax,     //@parm IN | Maximum number of items ever
    ULONG cbItem,       //@parm IN | Size of each item, in bytes
    ULONG cbPage        //@parm IN | Size of system page size (from SysInfo)
    )
{
    BYTE  *pb;

    m_cbReserved = ((cbItem *cItemMax) / cbPage + 1) *cbPage;
    m_rgItem = (BYTE *) VirtualAlloc( NULL, m_cbReserved, MEM_RESERVE, PAGE_READWRITE );

    if (m_rgItem == NULL)
        return ResultFromScode( E_OUTOFMEMORY );

    m_cbItem  = cbItem;
    m_dbAlloc = (cbItem / cbPage + 1) *cbPage;
    pb = (BYTE *) VirtualAlloc( m_rgItem, m_dbAlloc, MEM_COMMIT, PAGE_READWRITE );
    if (pb == NULL)
        {
        VirtualFree((VOID *) m_rgItem, 0, MEM_RELEASE );
        m_rgItem = NULL;
        return ResultFromScode( E_OUTOFMEMORY );
        }

    m_cbAlloc = m_dbAlloc;
    return ResultFromScode( S_OK );
}
```
Ejemplo en [ejemplos de Windows clásico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/dataaccess/oledb/sampprov/extbuff.cpp) en github.

## <a name="constants"></a>Constantes


| Constante o valor                                                                                                                                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_EXECUTE"></span><span id="page_execute"></span><dl> <dt>**Página \_ de EJECUTAR**</dt> <dt>0x10</dt> </dl>                                       | Habilita el acceso de ejecución a la región de páginas confirmada. Un intento de escribir en la región confirmada produce una infracción de acceso.<br/> Esta marca no es compatible con la función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="PAGE_EXECUTE_READ"></span><span id="page_execute_read"></span><dl> <dt>**Página \_ de EJECUTAR \_ Read**</dt> <dt>0x20</dt> </dl>                       | Habilita el acceso de ejecución o de solo lectura a la región de páginas confirmada. Un intento de escribir en la región confirmada produce una infracción de acceso.<br/> **Windows Server 2003 y Windows XP:** Este atributo no es compatible con la función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) hasta Windows XP con SP2 y windows Server 2003 con SP1.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="PAGE_EXECUTE_READWRITE"></span><span id="page_execute_readwrite"></span><dl> <dt>**Página \_ de EJECUTAR \_ ReadWrite**</dt> <dt>0x40</dt> </dl>        | Habilita el acceso de ejecución, de solo lectura o de lectura y escritura en la región de páginas confirmada.<br/> **Windows Server 2003 y Windows XP:** Este atributo no es compatible con la función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) hasta Windows XP con SP2 y windows Server 2003 con SP1.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="PAGE_EXECUTE_WRITECOPY"></span><span id="page_execute_writecopy"></span><dl> <dt>**Página \_ de EJECUTAR \_ WRITECOPY**</dt> <dt>0x80</dt> </dl>        | Habilita el acceso de ejecución, de solo lectura o de copia en escritura a una vista asignada de un objeto de asignación de archivos. Un intento de escribir en una página de copia en escritura confirmada tiene como resultado una copia privada de la página que se está realizando para el proceso. La página privada se marca como **Page \_ Execute \_ ReadWrite** y el cambio se escribe en la nueva página.<br/> Las funciones [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) o [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) no admiten esta marca. **Windows Vista, Windows Server 2003 y Windows XP:** Este atributo no es compatible con la función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) hasta Windows Vista con SP1 y windows Server 2008.<br/> <br/> |
| <span id="PAGE_NOACCESS"></span><span id="page_noaccess"></span><dl> <dt>**Página \_ de NoAccess**</dt> <dt>0x01</dt> </dl>                                    | Deshabilita el acceso a la región de páginas confirmada. Un intento de leer, escribir o ejecutar la región confirmada produce una infracción de acceso.<br/> Esta marca no es compatible con la función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="PAGE_READONLY"></span><span id="page_readonly"></span><dl> <dt>**Página \_ de SOLO lectura**</dt> <dt>0x02</dt> </dl>                                    | Habilita el acceso de solo lectura a la región de páginas confirmada. Un intento de escribir en la región confirmada produce una infracción de acceso. Si se habilita la [prevención de ejecución de datos](data-execution-prevention.md) , un intento de ejecutar código en la región confirmada produce una infracción de acceso.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="PAGE_READWRITE"></span><span id="page_readwrite"></span><dl> <dt>**Página \_ de READWRITE**</dt> <dt>0x04</dt> </dl>                                 | Habilita el acceso de solo lectura o de lectura y escritura en la región de páginas confirmada. Si se habilita la [prevención de ejecución de datos](data-execution-prevention.md) , si se intenta ejecutar código en la región confirmada, se producirá una infracción de acceso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="PAGE_WRITECOPY"></span><span id="page_writecopy"></span><dl> <dt>**Página \_ de WRITECOPY**</dt> <dt>0x08</dt> </dl>                                 | Habilita el acceso de solo lectura o de copia en escritura a una vista asignada de un objeto de asignación de archivos. Un intento de escribir en una página de copia en escritura confirmada tiene como resultado una copia privada de la página que se está realizando para el proceso. La página privada se marca como **\_ ReadWrite de página** y el cambio se escribe en la nueva página. Si se habilita la [prevención de ejecución de datos](data-execution-prevention.md) , si se intenta ejecutar código en la región confirmada, se producirá una infracción de acceso.<br/> Las funciones [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) o [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) no admiten esta marca.<br/>                                                                               |
| <span id="PAGE_TARGETS_INVALID"></span><span id="page_targets_invalid"></span><dl> <dt>**Página \_ de Tiene como destino un 0x40000000 \_ no válido**</dt> <dt></dt> </dl>        | Establece todas las ubicaciones de las páginas como destinos no válidos para CFG. Se usa junto con cualquier protección de página de ejecución, como **Page \_ Execute**, **Page \_ Execute \_ Read**, **Page \_ Execute \_ ReadWrite** y **Page \_ Execute \_ WRITECOPY**. Cualquier llamada indirecta a ubicaciones en esas páginas producirá un error en las comprobaciones de CFG y se terminará el proceso. El comportamiento predeterminado de las páginas ejecutables asignadas se marcará como destinos de llamada válidos para CFG.<br/> Esta marca no es compatible con las funciones [**VirtualProtect (**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) o [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                              |
| <span id="PAGE_TARGETS_NO_UPDATE"></span><span id="page_targets_no_update"></span><dl> <dt>**Página \_ de DESTINOS \_ sin \_ actualización**</dt> de <dt>0x40000000</dt> </dl> | No se actualizará la información de CFG de las páginas de la región mientras la protección cambia para [**VirtualProtect (**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect). Por ejemplo, si las páginas de la región se asignaron **con \_ destinos de página \_ no válidos**, la información no válida se mantendrá mientras se modifica la protección de la página. Esta marca solo es válida cuando la protección cambia a un tipo ejecutable, como **la \_ ejecución** de la página, la ejecución de la página **\_ \_ lectura**, la página ejecutar **\_ \_ ReadWrite** y la **página \_ ejecutar \_ WRITECOPY**. El comportamiento predeterminado para el cambio de protección de **VirtualProtect (** a ejecutable es marcar todas las ubicaciones como destinos de llamada válidos para cfg. <br/>                                           |



A continuación se muestran los modificadores que se pueden usar además de las opciones proporcionadas en la tabla anterior, excepto en los casos indicados.



| Constante o valor                                                                                                                                                                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_GUARD"></span><span id="page_guard"></span><dl> <dt>**Página \_ de GUARD**</dt> <dt>0x100</dt> </dl>                      | Las páginas de la región se convierten en páginas de protección. Cualquier intento de obtener acceso a una página de protección hace que el sistema genere una excepción de **\_ \_ \_ infracción** de la página de protección de estado y desactive el estado de la página de protección. Proteja las páginas, por lo que actúa como una alarma de acceso único. Para obtener más información, vea [Creating Guard Pages](creating-guard-pages.md) (Crear páginas de protección).<br/> Cuando un intento de acceso hace que el sistema desactive el estado de la página de protección, la protección de página subyacente toma el control.<br/> Si se produce una excepción de página de protección durante un servicio del sistema, el servicio devuelve normalmente un indicador de estado de error.<br/> Este valor no se puede usar con la **página \_ NoAccess**.<br/> Esta marca no es compatible con la función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                                                                                                                                              |
| <span id="PAGE_NOCACHE"></span><span id="page_nocache"></span><dl> <dt>**Página \_ de Nocache**</dt> <dt>0x200</dt> </dl>                | Establece que todas las páginas no sean cachable. Las aplicaciones no deben usar este atributo excepto cuando se requiere explícitamente para un dispositivo. El uso de las funciones de interbloqueos con la memoria que se asigna con **\_ nocache de sec** puede producir una excepción de **\_ \_ instrucción no válida** .<br/> La **marca Page \_ nocache** no se puede usar con las marcas Page **\_ Guard**, **Page \_ NoAccess** o **\_ WRITECOMBINE Page** .<br/> La **marca Page \_ nocache** solo se puede usar al asignar memoria privada con las funciones [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)o [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) . Para habilitar el acceso de memoria no almacenada en caché para la memoria compartida, especifique la marca **sec \_ nocache** al llamar a la función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                                                                   |
| <span id="PAGE_WRITECOMBINE"></span><span id="page_writecombine"></span><dl> <dt>**Página \_ de WRITECOMBINE**</dt> <dt>0x400</dt> </dl> | Establece todas las páginas que se van a combinar para escritura. <br/> Las aplicaciones no deben usar este atributo excepto cuando se requiere explícitamente para un dispositivo. El uso de las funciones entrelazadas con memoria asignada como combinación de escritura puede producir una excepción **de \_ \_ instrucción no válida** . <br/> No se puede especificar la marca **Page \_ WRITECOMBINE** con las marcas Page **\_ NoAccess**, Page **\_ Guard** y **Page \_ nocache** . <br/> La **marca \_ WRITECOMBINE** de la página solo se puede usar al asignar memoria privada con las funciones [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)o [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) . Para habilitar el acceso a la memoria combinada para escritura para la memoria compartida, especifique la marca **sec \_ WRITECOMBINE** cuando llame a la función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/> **Windows Server 2003 y Windows XP:** Esta marca no se admite hasta Windows Server 2003 con SP1.<br/> |



Las constantes siguientes solo se pueden usar con la función [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) cuando se especifica una enclave que tiene la arquitectura de las extensiones de software Guard de Intel (SGX).



| Constante                                                                                                                                                                                                  | Descripción                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_ENCLAVE_THREAD_CONTROL"></span><span id="page_enclave_thread_control"></span><dl> <dt>**\_control de \_ subproceso de enclave de página \_**</dt> </dl> | La página contiene una estructura de control de subprocesos (TCS).<br/>                                                                              |
| <span id="PAGE_ENCLAVE_UNVALIDATED"></span><span id="page_enclave_unvalidated"></span><dl> <dt>**PÁGINA \_ enclave no \_ validada**</dt> </dl>           | El contenido de la página que proporcione se excluye de la medida con la instrucción EEXTEND del modelo de programación de Intel SGX.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Winnt. h (incluye Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)
</dt> <dt>

[Protección de la memoria](memory-protection.md)
</dt> <dt>

[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
</dt> <dt>

[**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)
</dt> <dt>

[**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)
</dt> </dl>

 

 
