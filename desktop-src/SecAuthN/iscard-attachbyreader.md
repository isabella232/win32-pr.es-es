---
description: El método AttachByReader abre la tarjeta inteligente en el lector con nombre.
ms.assetid: a92f3281-5018-4e90-bfa0-f03eb9373bb1
title: 'ISCard:: AttachByReader (método) (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByReader
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2607ea2e13be2dcccc3c1b6beebd40c86822d0a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002754"
---
# <a name="iscardattachbyreader-method"></a>ISCard:: AttachByReader (método)

\[El método **AttachByReader** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **AttachByReader** abre la [*tarjeta inteligente*](../secgloss/s-gly.md) en el [*lector*](../secgloss/r-gly.md)con nombre.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AttachByReader(
  [in] BSTR              bstrReaderName,
  [in] SCARD_SHARE_MODES ShareMode,
  [in] SCARD_PROTOCOLS   PrefProtocol
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrReaderName* \[ de\]
</dt> <dd>

**BSTR** que contiene el nombre del lector de tarjeta inteligente.

</dd> <dt>

*ShareMode* \[ de\]
</dt> <dd>

Modo en el que se va a notificar el acceso a la tarjeta inteligente.



| Value                                                                                                                                            | Significado                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**ÚNICO**</dt> </dl> | Nadie más usa esta conexión con la tarjeta inteligente.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**RECURSO**</dt> </dl>          | Otras aplicaciones pueden usar esta conexión.<br/>        |



 

</dd> <dt>

*PrefProtocol* \[ de\]
</dt> <dd>

Valor de protocolo preferido.

<dl><span id="T0"></span><span id="t0"></span><dt>

**T0**
</dt><span id="T1"></span><span id="t1"></span><dt>

**T1**
</dt><span id="RAW"></span><span id="raw"></span><dt>

**RAW**
</dt><span id="T0_T1"></span><span id="t0_t1"></span><dt>

**T0 \| T1**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                  | Descripción                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Abrir en la tarjeta inteligente en el lector con nombre se ha completado correctamente.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Hay un problema con uno o varios de los parámetros pasados a la función.<br/> |



 

## <a name="remarks"></a>Observaciones

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

Cuando haya terminado de usar el lector, libere los datos adjuntos llamando al método [**ISCard::D Etach**](iscard-detach.md) .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo conectarse a una tarjeta inteligente en un lector de tarjeta inteligente especificado.


```C++
#include <windows.h>
#include <stdio.h>
#include <Scardmgr.h>

// The reader name is vendor specific; change as needed.
#define READER_NAME L"Vendor Reader 0"

void main()
{
    BSTR     bstrReader = NULL;
    HRESULT  hr;

    bstrReader = SysAllocString(READER_NAME);
    if (NULL == bstrReader)
    {
        // Error encountered.
        exit(1);
    }

    // Connect to the reader.
    hr = pISCard->AttachByReader(bstrReader, SHARED, T0);
    if (FAILED(hr))
    {
        printf("Failed AttachByReader\n");
        // Take other error handling action.
        // ...
    }

    // Detach reader by calling ISCard::Detach (not shown).
    // ...

    // When done, free BSTR.
    if (NULL != bstrReader)
        SysFreeString(bstrReader);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**Conecta**](iscard-detach.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**Volver a adjuntar**](iscard-reattach.md)
</dt> </dl>

 

 
