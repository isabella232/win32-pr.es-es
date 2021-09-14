---
description: El método SWbemRefresher.Add agrega un nuevo objeto SWbemRefreshableItem a la colección del objeto SWbemRefresher. Objeto SWbemRefreshableItem a la colección del objeto SWbemRefresher.
ms.assetid: 92d11a18-1eed-4958-b74a-2f9de4907dd0
ms.tgt_platform: multiple
title: Método SWbemRefresher.Add (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Add
- ISWbemRefresher.Add
- ISWbemRefresher.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ebe9da221314252b2b143bf674cd7bb7177329b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070378"
---
# <a name="swbemrefresheradd-method"></a>Método SWbemRefresher.Add

El **método SWbemRefresher.Add** agrega un nuevo objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) a la colección del [**objeto SWbemRefresher.**](swbemrefresher.md)

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objRefreshItem = .Add( _
  ByVal objWbemService, _
  ByVal strInstancePath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*objWbemService* 
</dt> <dd>

Necesario. Objeto [**SWbemServices**](swbemservices.md) que representa una conexión al espacio de nombres en el que reside el objeto que se agrega al actualizador.

</dd> <dt>

*strInstancePath* 
</dt> <dd>

Necesario. Cadena que contiene la ruta de acceso relativa del objeto en el espacio de nombres . La ruta de acceso debe contener una instancia de . La [**propiedad Index**](swbemrefreshableitem-index.md) del objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) devuelto representa el índice del objeto en la colección del actualizador.

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Cadena que contiene la ruta de acceso del objeto para el que se ejecuta el método.

</dd> <dt>

*objWbemNamedvalueSet* \[ Opcional\]
</dt> <dd>

Normalmente, esto no está definido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que proporciona servicios a la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la llamada se realiza correctamente, se devuelve un objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) que contiene un único objeto actualizable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemRefresher<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




