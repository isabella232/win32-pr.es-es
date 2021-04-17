---
description: Muestra una interfaz de usuario seleccionada que permite seleccionar un nombre de usuario.
ms.assetid: 0a02d9e5-b2cf-4818-a2e1-89e6019e53d4
title: 'ISCrdEnr:: selectUserName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectUserName
- SCrdEnr.selectUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 13059775abc8520c39a0ad3dea2d604fc8d65455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668332"
---
# <a name="iscrdenrselectusername-method"></a>ISCrdEnr:: selectUserName (método)

El método **selectUserName** muestra una interfaz de **usuario** seleccionada que permite seleccionar un nombre de usuario.

El nombre de usuario se aplica al usuario en cuyo nombre está diseñada la inscripción de certificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT selectUserName(
  [in] DWORD dwFlags
);
```


```VB

SCrdEnr.selectUserName( _
  ByVal dwFlags _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Reservado para uso futuro. Establezca este valor en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="vb"></a>VB

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

## <a name="remarks"></a>Observaciones

Use este método para seleccionar el nombre del usuario. Una vez que se ha seleccionado un nombre de usuario, su valor se puede recuperar llamando al método [**ISCrdEnr:: getUserName**](iscrdenr-getusername.md) .

Una alternativa al uso de la interfaz ' Select User ' consiste en especificar un usuario mediante una llamada al método [**ISCrdEnr:: setUserName**](iscrdenr-setusername.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr:: getUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**ISCrdEnr:: resetuser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 




