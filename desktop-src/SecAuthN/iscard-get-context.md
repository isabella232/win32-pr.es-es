---
description: Recupera el identificador de contexto del administrador de recursos actual. Este método devuelve ( \* pContext) = = NULL si no se ha establecido ningún contexto.
ms.assetid: c031f53d-4670-4d48-934c-a1550f21c23a
title: 'Método ISCard:: get_Context (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Context
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8b5aba075d755b644a78cca23a827a70966f4ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912469"
---
# <a name="iscardget_context-method"></a>ISCard:: get ( \_ método de contexto)

\[El método de **\_ contexto Get** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método de **\_ contexto Get** recupera el identificador de [*contexto del administrador de recursos*](../secgloss/r-gly.md) actual. Este método devuelve ( \* *pContext*) = = **null** si no se ha establecido ningún contexto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Context(
  [out] HSCARDCONTEXT *pContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContext* \[ enuncia\]
</dt> <dd>

Puntero al identificador de contexto en la devolución.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                  | Descripción                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Operación completada correctamente.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro *pContext* no es válido.<br/>  |
| <dl> <dt>**\_puntero E**</dt> </dl>    | Se pasó un puntero incorrecto en *pContext*.<br/> |



 

## <a name="remarks"></a>Observaciones

El contexto del administrador de recursos se establece mediante una llamada a la función de [*tarjeta inteligente*](../secgloss/s-gly.md) [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo recuperar el identificador de [*contexto del administrador de recursos*](../secgloss/r-gly.md) actual.


```C++
HSCARDCONTEXT  hCtx;
HRESULT        hr;

// Retrieve the smart card context.
hr = pISCard->get_Context(&hCtx);
if (FAILED(hr))
{
   printf("Failed get_Context\n");
   // Take other error handling action as needed.
}
// Use smart card context as needed.
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

[**obtener \_ ATR**](iscard-get-atr.md)
</dt> <dt>

[**obtener \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**obtener \_ Protocolo**](iscard-get-protocol.md)
</dt> <dt>

[**obtener \_ Estado**](iscard-get-status.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)
</dt> </dl>

 

 
