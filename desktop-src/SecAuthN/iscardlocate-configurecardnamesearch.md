---
description: El método ConfigureCardNameSearch especifica los nombres de tarjeta que se van a usar en la búsqueda de la tarjeta inteligente.
ms.assetid: fb406696-0cf0-4d67-8125-8888ee1b8213
title: 'ISCardLocate:: ConfigureCardNameSearch (método) (Scardmgr. h)'
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
ms.openlocfilehash: 4af451bea1f08df2af0a673b26e84c9df2a0954b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277340"
---
# <a name="iscardlocateconfigurecardnamesearch-method"></a>ISCardLocate:: ConfigureCardNameSearch (método)

\[El método **ConfigureCardNameSearch** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **ConfigureCardNameSearch** especifica los nombres de tarjeta que se van a usar en la búsqueda de la [*tarjeta inteligente*](../secgloss/s-gly.md).

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

*pCardNames* \[ de\]
</dt> <dd>

Puntero a una matriz segura de automatización de nombres de tarjeta en formato BSTR.

</dd> <dt>

*pGroupNames* \[ de\]
</dt> <dd>

Puntero a una matriz segura de automatización de nombres de grupos de tarjetas o lectores en formato BSTR que se va a agregar a la búsqueda.

</dd> <dt>

*bstrTitle* \[ de\]
</dt> <dd>

Título del cuadro de diálogo para el control común de búsqueda.

</dd> <dt>

*lFlags* \[ de\]
</dt> <dd>

Especifica cuándo se muestra la [*interfaz de usuario*](../secgloss/u-gly.md) .



| Value                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**\_interfaz de \_ \_ usuario mínima de SC Dlg**</dt> </dl> | Muestra el cuadro de diálogo solo si la tarjeta que se está buscando en la aplicación que realiza la llamada no está ubicada y disponible para su uso en un lector. Esto permite que la tarjeta se encuentre, conectada (ya sea a través de un mecanismo de cuadros de diálogo interno o mediante las funciones de devolución de llamada de usuario) y se devuelva a la aplicación que realiza la llamada.<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ Dlg \_ sin \_ interfaz de usuario**</dt> </dl>                | No provoca ninguna presentación de la interfaz de usuario, independientemente del resultado de la búsqueda.<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**fuerza de IU de SC \_ Dlg \_ \_**</dt> </dl>       | Provoca la presentación de la interfaz de usuario independientemente del resultado de la búsqueda.<br/>                                                                                                                                                                                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                                           |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                                         |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido en *pCardNames* o *pGroupNames*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                                             |



 

## <a name="remarks"></a>Observaciones

Para buscar la [*tarjeta inteligente*](../secgloss/s-gly.md), llame a [**FindCard**](iscardlocate-findcard.md).

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardLocate**](iscardlocate.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

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
| IID<br/>                      | IID \_ ISCardLocate se define como 1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FindCard**](iscardlocate-findcard.md)
</dt> <dt>

[**ISCardLocate**](iscardlocate.md)
</dt> </dl>

 

 
