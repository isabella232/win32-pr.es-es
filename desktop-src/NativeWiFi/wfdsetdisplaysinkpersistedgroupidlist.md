---
description: Establece la lista de identificadores de grupo persistentes para todos los perfiles que la aplicación conserva.
ms.assetid: EF83F295-CD53-45A4-B209-560B4069CA7C
title: Función WFDDisplaySinkSetPersistedGroupIDList (Wfdsink.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDSetDisplaySinkPersistedGroupIDList
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423360d7127f331fd1aa2de7f7370daebcc2b417
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473741"
---
# <a name="wfddisplaysinksetpersistedgroupidlist-function"></a>Función WFDDisplaySinkSetPersistedGroupIDList

Establece la lista de identificadores de grupo persistentes para todos los perfiles que la aplicación conserva. La aplicación debe llamar a este método cada vez que agrega o elimina un perfil de su almacenamiento.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI WFDSetDisplaySinkPersistedGroupIDList(
  _In_ UINT32             cGroupIDList,
  _In_ DOT11_WFD_GROUP_ID *pGroupIDList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cGroupIDList* \[ En\]
</dt> <dd>

Recuento de identificadores de grupo a los que apunta *pGroupIDList.*

</dd> <dt>

*pGroupIDList* \[ En\]
</dt> <dd>

Puntero a una matriz de identificadores de grupo *cGroupIDList.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

## <a name="remarks"></a>Observaciones

Siempre se espera que se llame a este método con toda la lista y no con un subconjunto. Es correcto llamar a este método con 0 perfiles cuando el almacén de perfiles está vacío.

Se producirá un error al volver a invocar para un identificador de grupo que no forma parte de la lista proporcionada. grupo P2P desconocido"(estado 8).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows 10<br/>                                                                      |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2016<br/>                                                             |
| Encabezado<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wifidisplay.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



 

 




