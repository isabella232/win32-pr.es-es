---
description: El método FindCard busca la tarjeta inteligente y abre una conexión válida a ella.
ms.assetid: ab97eff2-0f41-4a6f-98b3-d5ad5883fa07
title: Método ISCardLocate::FindCard (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.FindCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bf3cf05ff6e6040d5cac2bde161fa2eea07d5297
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244227"
---
# <a name="iscardlocatefindcard-method"></a>Método ISCardLocate::FindCard

\[El **método FindCard** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método FindCard** busca la [*tarjeta inteligente y*](../secgloss/s-gly.md) abre una conexión válida a ella.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindCard(
  [in]  SCARD_SHARE_MODES ShareMode,
  [in]  SCARD_PROTOCOLS   Protocols,
  [in]  LONG              lFlags,
  [out] LPSCARDINFO       *ppCardInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ShareMode* \[ En\]
</dt> <dd>

Modo en el que se va a compartir o no la tarjeta inteligente cuando se abre una conexión a ella.



| Value                                                                                                                                            | Significado                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**EXCLUSIVO**</dt> </dl> | Nadie más usa esta conexión a la tarjeta inteligente.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**COMPARTIDO**</dt> </dl>          | Otras aplicaciones pueden usar esta conexión.<br/>        |



 

</dd> <dt>

*Protocolos* \[ En\]
</dt> <dd>

Protocolo que se usará al conectarse a la tarjeta.

T0

T1

RAW

T0 \| T1

</dd> <dt>

*lFlags* \[ En\]
</dt> <dd>

Especifica cuándo se [*muestra la interfaz*](../secgloss/u-gly.md) de usuario:



| Value                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**INTERFAZ \_ DE USUARIO MÍNIMA DE SC DLG \_ \_**</dt> </dl> | Muestra el cuadro de diálogo solo si la tarjeta que busca la aplicación que realiza la llamada no se encuentra y está disponible para su uso en un lector. Esto permite que la tarjeta se encuentra, se conecta (ya sea a través de un mecanismo de cuadro de diálogo interno o mediante las funciones de devolución de llamada del usuario) y se devuelve a la aplicación que realiza la llamada.<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ DLG \_ NO \_ UI**</dt> </dl>                | No provoca ninguna presentación de la interfaz de usuario, independientemente del resultado de la búsqueda.<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**INTERFAZ \_ DE USUARIO DE SC DLG \_ FORCE \_**</dt> </dl>       | Hace que la interfaz de usuario se muestre independientemente del resultado de la búsqueda.<br/>                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*ppCardInfo* \[ out\]
</dt> <dd>

Puntero a un puntero a una estructura de datos que contiene o devuelve información sobre la tarjeta [*inteligente abierta,*](../secgloss/s-gly.md)si se realiza correctamente. Será **NULL si se** ha dado error en la operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                        |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido *en ppCardInfo*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                            |



 

## <a name="remarks"></a>Observaciones

Para establecer los criterios de búsqueda de la búsqueda, llame a [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) para especificar los nombres de tarjeta de una tarjeta inteligente.

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardLocate**](iscardlocate.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardLocate se define como \_ 1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md)
</dt> <dt>

[**ISCardLocate**](iscardlocate.md)
</dt> </dl>

 

 
