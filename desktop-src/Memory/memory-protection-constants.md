---
Description: Estas son las opciones de protección de memoria; Debe especificar uno de los siguientes valores al asignar o proteger una página en memoria. Los atributos de protección no se pueden asignar a una parte de una página; solo se pueden asignar a una página completa.
ms.assetid: 09839db7-2118-4a7d-a707-a08c92bd600c
title: Constantes de protección de memoria (WinNT.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 641fab68024d9db96f50327f7c78d51f3f9bca01
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159829"
---
# <a name="memory-protection-constants"></a>Constantes de protección de memoria

Estas son las opciones de protección de memoria; Debe especificar uno de los siguientes valores al asignar o proteger una página en memoria. Los atributos de protección no se pueden asignar a una parte de una página; solo se pueden asignar a una página completa.

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
Por ejemplo, [Windows ejemplos clásicos](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/dataaccess/oledb/sampprov/extbuff.cpp) en GitHub.

## <a name="constants"></a>Constantes


| Constante o valor                                                                                                                                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_EXECUTE"></span><span id="page_execute"></span><dl> <dt>**PÁGINA \_ EXECUTE**</dt> <dt>0x10</dt> </dl>                                       | Habilita el acceso de ejecución a la región de páginas que se ha confirmado. Un intento de escribir en la región confirmada produce una infracción de acceso.<br/> Esta marca no es compatible con la [**función CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="PAGE_EXECUTE_READ"></span><span id="page_execute_read"></span><dl> <dt>**PÁGINA \_ EXECUTE \_ READ**</dt> <dt>0x20</dt> </dl>                       | Habilita el acceso de ejecución o de solo lectura a la región de páginas que se ha confirmado. Un intento de escribir en la región confirmada produce una infracción de acceso.<br/> **Windows Server 2003 y Windows XP:** La función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) no admite este atributo hasta Windows XP con SP2 y Windows Server 2003 con SP1.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="PAGE_EXECUTE_READWRITE"></span><span id="page_execute_readwrite"></span><dl> <dt>**PÁGINA \_ EXECUTE \_ READWRITE**</dt> <dt>0x40</dt> </dl>        | Habilita el acceso de ejecución, de solo lectura o de lectura y escritura a la región de páginas que se ha confirmado.<br/> **Windows Server 2003 y Windows XP:** La función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) no admite este atributo hasta Windows XP con SP2 y Windows Server 2003 con SP1.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="PAGE_EXECUTE_WRITECOPY"></span><span id="page_execute_writecopy"></span><dl> <dt>**PÁGINA \_ EXECUTE \_ WRITECOPY**</dt> <dt>0x80</dt> </dl>        | Habilita el acceso de ejecución, solo lectura o copia en escritura a una vista asignada de un objeto de asignación de archivos. Un intento de escribir en una página de copia en escritura confirmado da como resultado una copia privada de la página que se realiza para el proceso. La página privada está marcada como **PAGE \_ EXECUTE \_ READWRITE** y el cambio se escribe en la nueva página.<br/> Las funciones [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) o [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) no admiten esta marca. **Windows Vista, Windows Server 2003 y Windows XP:** La función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) no admite este atributo hasta Windows Vista con SP1 y Windows Server 2008.<br/> <br/> |
| <span id="PAGE_NOACCESS"></span><span id="page_noaccess"></span><dl> <dt>**PÁGINA \_ Noaccess**</dt> <dt>0x01</dt> </dl>                                    | Deshabilita todo el acceso a la región de páginas que se ha confirmado. Un intento de leer, escribir o ejecutar la región confirmada produce una infracción de acceso.<br/> Esta marca no es compatible con la [**función CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="PAGE_READONLY"></span><span id="page_readonly"></span><dl> <dt>**PÁGINA \_ ReadONLY**</dt> <dt>0x02</dt> </dl>                                    | Habilita el acceso de solo lectura a la región de páginas que se ha confirmado. Un intento de escribir en la región confirmada produce una infracción de acceso. Si [la prevención de ejecución](data-execution-prevention.md) de datos está habilitada, un intento de ejecutar código en la región confirmada produce una infracción de acceso.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="PAGE_READWRITE"></span><span id="page_readwrite"></span><dl> <dt>**PÁGINA \_ ReadWRITE**</dt> <dt>0x04</dt> </dl>                                 | Habilita el acceso de solo lectura o de lectura y escritura a la región de páginas que se ha confirmado. Si [la prevención de ejecución](data-execution-prevention.md) de datos está habilitada, el intento de ejecutar código en la región confirmada produce una infracción de acceso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="PAGE_WRITECOPY"></span><span id="page_writecopy"></span><dl> <dt>**PÁGINA \_ WriteCOPY**</dt> <dt>0x08</dt> </dl>                                 | Habilita el acceso de solo lectura o de copia en escritura a una vista asignada de un objeto de asignación de archivos. Un intento de escribir en una página de copia en escritura confirmado da como resultado una copia privada de la página que se realiza para el proceso. La página privada está marcada como **PAGE \_ READWRITE** y el cambio se escribe en la nueva página. Si [la prevención de ejecución](data-execution-prevention.md) de datos está habilitada, el intento de ejecutar código en la región confirmada produce una infracción de acceso.<br/> Las funciones [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) o [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) no admiten esta marca.<br/>                                                                               |
| <span id="PAGE_TARGETS_INVALID"></span><span id="page_targets_invalid"></span><dl> <dt>**PÁGINA \_ DESTINOS \_ NO VÁLIDOS**</dt> <dt>0x40000000</dt> </dl>        | Establece todas las ubicaciones de las páginas como destinos no válidos para CFG. Se usa junto con cualquier protección de página de ejecución como **PAGE \_ EXECUTE**, **PAGE EXECUTE \_ \_ READ**, **PAGE EXECUTE \_ \_ READWRITE** **y PAGE EXECUTE \_ \_ WRITECOPY**. Cualquier llamada indirecta a ubicaciones de esas páginas producirá un error en las comprobaciones de CFG y el proceso finalizará. El comportamiento predeterminado de las páginas ejecutables asignadas es que se marquen destinos de llamada válidos para CFG.<br/> Las funciones [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) o [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) no admiten esta marca.<br/>                                                                                                              |
| <span id="PAGE_TARGETS_NO_UPDATE"></span><span id="page_targets_no_update"></span><dl> <dt>**PÁGINA \_ NO \_ TIENE COMO DESTINO NINGUNA \_ actualización**</dt> <dt>0x40000000</dt> </dl> | Las páginas de la región no tendrán su información de CFG actualizada mientras la protección cambia para [**VirtualProtect.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) Por ejemplo, si las páginas de la región se asignaron mediante **PAGE \_ TARGETS \_ INVALID**, la información no válida se mantendrá mientras cambia la protección de la página. Esta marca solo es válida cuando la protección cambia a un tipo ejecutable como **PAGE \_ EXECUTE**, **PAGE EXECUTE \_ \_ READ,** **PAGE EXECUTE READ \_ \_ Y** **PAGE EXECUTE \_ \_ WRITECOPY.** El comportamiento predeterminado para **el cambio de protección de VirtualProtect** a ejecutable es marcar todas las ubicaciones como destinos de llamada válidos para CFG. <br/>                                           |



Los siguientes son modificadores que se pueden usar además de las opciones proporcionadas en la tabla anterior, excepto como se indicó.



| Constante o valor                                                                                                                                                                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_GUARD"></span><span id="page_guard"></span><dl> <dt>**PÁGINA \_ Protección**</dt> <dt>0x100</dt> </dl>                      | Las páginas de la región se convierten en páginas de protección. Cualquier intento de acceder a una página de protección hace que el sistema genera una excepción DE INFRACCIÓN DE PÁGINA DE PROTECCIÓN DE ESTADO y desactiva el estado de la página de protección. **\_ \_ \_** Por lo tanto, las páginas de protección actúan como una alarma de acceso única. Para obtener más información, vea [Creating Guard Pages](creating-guard-pages.md) (Crear páginas de protección).<br/> Cuando un intento de acceso lleva al sistema a desactivar el estado de la página de protección, la protección de página subyacente toma el control.<br/> Si se produce una excepción de página de protección durante un servicio del sistema, el servicio normalmente devuelve un indicador de estado de error.<br/> Este valor no se puede usar con **PAGE \_ NOACCESS.**<br/> Esta marca no es compatible con la [**función CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                              |
| <span id="PAGE_NOCACHE"></span><span id="page_nocache"></span><dl> <dt>**PÁGINA \_ Nocache**</dt> <dt>0x200</dt> </dl>                | Establece todas las páginas para que no sean cachables. Las aplicaciones no deben usar este atributo excepto cuando se requiere explícitamente para un dispositivo. El uso de las funciones entrelazados con memoria asignada a **\_ SEC NOCACHE** puede dar lugar a una **excepción EXCEPTION ILLEGAL \_ \_ INSTRUCTION.**<br/> La **marca PAGE \_ NOCACHE** no se puede usar con las marcas **PAGE \_ GUARD**, **PAGE \_ NOACCESS** o **PAGE \_ WRITECOMBINE.**<br/> La **marca PAGE \_ NOCACHE** solo se puede usar al asignar memoria privada con las funciones [**VirtualAlloc,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)o [**VirtualAllocExNuma.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) Para habilitar el acceso a memoria no almacenada en caché para la memoria compartida, especifique la marca **\_ SEC NOCACHE** al llamar a la [**función CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                   |
| <span id="PAGE_WRITECOMBINE"></span><span id="page_writecombine"></span><dl> <dt>**PÁGINA \_ WRITECOMBINE**</dt> <dt>0x400</dt> </dl> | Establece todas las páginas que se combinarán con escritura. <br/> Las aplicaciones no deben usar este atributo excepto cuando se requiere explícitamente para un dispositivo. El uso de las funciones entrelazados con memoria asignada como combinación de escritura puede dar lugar a una **excepción EXCEPTION \_ ILLEGAL \_ INSTRUCTION.** <br/> La **marca \_ PAGE WRITECOMBINE** no se puede especificar con las marcas **PAGE \_ NOACCESS,** **PAGE \_ GUARD** y **PAGE \_ NOCACHE.** <br/> La **marca \_ PAGE WRITECOMBINE** solo se puede usar al asignar memoria privada con las funciones [**VirtualAlloc,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)o [**VirtualAllocExNuma.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) Para habilitar el acceso de memoria combinada de escritura para la memoria compartida, especifique la marca **\_ WRITECOMBINE de SEC** al llamar a la función [**CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/> **Windows Server 2003 y Windows XP:** Esta marca no se admite hasta Windows Server 2003 con SP1.<br/> |



Las siguientes constantes solo se pueden usar con la función [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) cuando se especifica un enclave que tiene la arquitectura intel Software Guard Extensions (SGX).



| Constante                                                                                                                                                                                                  | Descripción                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_ENCLAVE_THREAD_CONTROL"></span><span id="page_enclave_thread_control"></span><dl> <dt>**PAGE \_ ENCLAVE \_ THREAD \_ CONTROL**</dt> </dl> | La página contiene una estructura de control de subprocesos (TCS).<br/>                                                                              |
| <span id="PAGE_ENCLAVE_UNVALIDATED"></span><span id="page_enclave_unvalidated"></span><dl> <dt>**ENCLAVE \_ DE PÁGINA SIN \_ VALIDAR**</dt> </dl>           | El contenido de la página que proporcione se excluye de la medida con la instrucción EEXTEND del modelo de programación Intel SGX.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>WinNT.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 
