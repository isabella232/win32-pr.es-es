---
description: Agrega un nuevo enumerador al objeto SWbemRefresher. Este enumerador es para todas las instancias de la clase especificada en el parámetro strClass.
ms.assetid: 0fa22a47-4050-43ae-aad3-3a8ebbf5e9b2
ms.tgt_platform: multiple
title: Método SWbemRefresher.AddEnum (Wbemdisp.h)
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
ms.openlocfilehash: 82b6ba19bf309db53a0c175a0e5e46498e3fb47c8a2bc6c443662b9dff16067d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117921802"
---
# <a name="swbemrefresheraddenum-method"></a>Método SWbemRefresher.AddEnum

El **método SWbemRefresher.AddEnum** agrega un nuevo enumerador al [**objeto SWbemRefresher.**](swbemrefresher.md) Este enumerador es para todas las instancias de la clase especificada en el *parámetro strClass.*

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

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

Obligatorio. Objeto [**SWbemServices**](swbemservices.md) que representa una conexión al espacio de nombres en el que reside el objeto que se agrega al actualizador.

</dd> <dt>

*strClass* 
</dt> <dd>

Obligatorio. Cadena que contiene la clase que se agrega al actualizador. Esta clase se usa como enumerador de las instancias de la clase . La [**propiedad Index**](swbemrefreshableitem-index.md) del objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) devuelto representa el índice del enumerador en la colección del actualizador.

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

Si la llamada se realiza correctamente, se devuelve un objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) que contiene un enumerador para todas las instancias de la clase especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemRefresher<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




