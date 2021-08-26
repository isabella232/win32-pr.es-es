---
description: El método ConfigureCardNameSearch especifica los nombres de tarjeta que se usarán en la búsqueda de la tarjeta inteligente.
ms.assetid: fb406696-0cf0-4d67-8125-8888ee1b8213
title: Método ISCardLocate::ConfigureCardNameSearch (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.ConfigureCardNameSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e49b7653a434f54bfa706aea0bde63048d6b511e5143ade34f0b4e8225a6042b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014275"
---
# <a name="iscardlocateconfigurecardnamesearch-method"></a>Método ISCardLocate::ConfigureCardNameSearch

\[El **método ConfigureCardNameSearch** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método ConfigureCardNameSearch** especifica los nombres de tarjeta que se usarán en la búsqueda de [*la tarjeta inteligente.*](../secgloss/s-gly.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConfigureCardNameSearch(
  [in] LPSAFEARRAY pCardNames,
  [in] LPSAFEARRAY pGroupNames,
  [in] BSTR        bstrTitle,
  [in] LONG        lFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCardNames* \[ En\]
</dt> <dd>

Puntero a una matriz segura de automation de nombres de tarjeta en formato BSTR.

</dd> <dt>

*pGroupNames* \[ En\]
</dt> <dd>

Puntero a una matriz segura de Automation de nombres de grupos de tarjetas o lectores en formato BSTR que se va a agregar a la búsqueda.

</dd> <dt>

*bstrTitle* \[ En\]
</dt> <dd>

Título del cuadro de diálogo para el control común de búsqueda.

</dd> <dt>

*lFlags* \[ En\]
</dt> <dd>

Especifica cuándo [*se muestra la*](../secgloss/u-gly.md) interfaz de usuario.



| Value                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**INTERFAZ \_ DE USUARIO MÍNIMA DE SC DLG \_ \_**</dt> </dl> | Muestra el cuadro de diálogo solo si la tarjeta que la aplicación que realiza la llamada no se encuentra y está disponible para su uso en un lector. Esto permite encontrar la tarjeta, conectarse (a través de un mecanismo de cuadro de diálogo interno o mediante las funciones de devolución de llamada del usuario) y devolverla a la aplicación que realiza la llamada.<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ DLG \_ NO \_ UI**</dt> </dl>                | No provoca ninguna presentación de la interfaz de usuario, independientemente del resultado de la búsqueda.<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**SC \_ DLG \_ FORCE \_ UI**</dt> </dl>       | Hace que la interfaz de usuario se muestre independientemente del resultado de la búsqueda.<br/>                                                                                                                                                                                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                                           |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                                         |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido *en pCardNames* o *pGroupNames.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                                             |



 

## <a name="remarks"></a>Comentarios

Para buscar la [*tarjeta inteligente,*](../secgloss/s-gly.md)llame a [**FindCard**](iscardlocate-findcard.md).

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardLocate**](iscardlocate.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardLocate se define como \_ 1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FindCard**](iscardlocate-findcard.md)
</dt> <dt>

[**ISCardLocate**](iscardlocate.md)
</dt> </dl>

 

 
