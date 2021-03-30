---
description: Agrega un nuevo enumerador al objeto SWbemRefresher. Este enumerador es para todas las instancias de la clase que se especifica en el parámetro strClass.
ms.assetid: 0fa22a47-4050-43ae-aad3-3a8ebbf5e9b2
ms.tgt_platform: multiple
title: Método SWbemRefresher. AddEnum (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cffa406a3a45869038f5e6fed12b23b6b84fde27
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820223"
---
# <a name="swbemrefresheraddenum-method"></a>SWbemRefresher. AddEnum, método

El método **SWbemRefresher. AddEnum** agrega un nuevo enumerador al objeto [**SWbemRefresher**](swbemrefresher.md) . Este enumerador es para todas las instancias de la clase que se especifica en el parámetro *strClass* .

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objRefreshEnum = .AddEnum( _
  ByVal objWbemService, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*objWbemService* 
</dt> <dd>

Obligatorio. Un objeto [**SWbemServices**](swbemservices.md) que representa una conexión con el espacio de nombres en el que reside el objeto que se va a agregar al actualizador.

</dd> <dt>

*strClass* 
</dt> <dd>

Obligatorio. Cadena que contiene la clase que se va a agregar al actualizador. Esta clase se usa como un enumerador de las instancias de la clase. La propiedad [**index**](swbemrefreshableitem-index.md) del [**SWbemRefreshableItem**](swbemrefreshableitem.md) devuelto representa el índice del enumerador en la colección de actualizador.

</dd> <dt>

*iFlags* \[ opta\]
</dt> <dd>

Cadena que contiene la ruta de acceso del objeto para el que se ejecuta el método.

</dd> <dt>

*objWbemNamedvalueSet* \[ opta\]
</dt> <dd>

Normalmente, esto no está definido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que presta servicio a la solicitud. Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la llamada se realiza correctamente, se devuelve un objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) que contiene un enumerador para todas las instancias de la clase especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | \_ISWBEMREFRESHER IID<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




