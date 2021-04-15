---
description: El método FindCard busca la tarjeta inteligente y abre una conexión válida con ella.
ms.assetid: ab97eff2-0f41-4a6f-98b3-d5ad5883fa07
title: 'ISCardLocate:: FindCard (método) (Scardmgr. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648371"
---
# <a name="iscardlocatefindcard-method"></a>ISCardLocate:: FindCard (método)

\[El método **FindCard** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **FindCard** busca la [*tarjeta inteligente*](../secgloss/s-gly.md) y abre una conexión válida con ella.

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

*ShareMode* \[ de\]
</dt> <dd>

Modo en el que se va a compartir o no la tarjeta inteligente cuando se abre una conexión a ella.



| Value                                                                                                                                            | Significado                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**ÚNICO**</dt> </dl> | Nadie más usa esta conexión con la tarjeta inteligente.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**RECURSO**</dt> </dl>          | Otras aplicaciones pueden usar esta conexión.<br/>        |



 

</dd> <dt>

*Protocolos* \[ de de\]
</dt> <dd>

Protocolo que se utilizará al conectarse a la tarjeta.

T0

T1

RAW

T0 \| T1

</dd> <dt>

*lFlags* \[ de\]
</dt> <dd>

Especifica cuándo se muestra la [*interfaz de usuario*](../secgloss/u-gly.md) :



| Value                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**\_interfaz de \_ \_ usuario mínima de SC Dlg**</dt> </dl> | Muestra el cuadro de diálogo solo si la tarjeta que se está buscando en la aplicación que realiza la llamada no está ubicada y disponible para su uso en un lector. Esto permite que la tarjeta se encuentre, conectada (ya sea a través de un mecanismo de cuadros de diálogo interno o mediante las funciones de devolución de llamada de usuario) y se devuelva a la aplicación que realiza la llamada.<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ Dlg \_ sin \_ interfaz de usuario**</dt> </dl>                | No provoca ninguna presentación de la interfaz de usuario, independientemente del resultado de la búsqueda.<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**fuerza de IU de SC \_ Dlg \_ \_**</dt> </dl>       | Provoca la presentación de la interfaz de usuario independientemente del resultado de la búsqueda.<br/>                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*ppCardInfo* \[ enuncia\]
</dt> <dd>

Puntero a un puntero a una estructura de datos que contiene o devuelve información acerca de la [*tarjeta inteligente*](../secgloss/s-gly.md)abierta, si se realiza correctamente. Será **null** si se produce un error en la operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                        |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido en *ppCardInfo*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                            |



 

## <a name="remarks"></a>Observaciones

Para establecer los criterios de búsqueda de la búsqueda, llame a [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) para especificar los nombres de tarjeta de una tarjeta inteligente.

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

[**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md)
</dt> <dt>

[**ISCardLocate**](iscardlocate.md)
</dt> </dl>

 

 
