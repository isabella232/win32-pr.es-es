---
description: Muestra una interfaz Seleccionar usuario, lo que permite seleccionar un nombre de usuario.
ms.assetid: 0a02d9e5-b2cf-4818-a2e1-89e6019e53d4
title: Método ISCrdEnr::selectUserName
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170977"
---
# <a name="iscrdenrselectusername-method"></a>Método ISCrdEnr::selectUserName

El **método selectUserName** muestra una **interfaz Seleccionar** usuario, lo que permite seleccionar un nombre de usuario.

El nombre de usuario se aplica al usuario en cuyo nombre está prevista la inscripción del certificado.

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

*dwFlags* \[ En\]
</dt> <dd>

Reservado para uso futuro. Establezca este valor en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="vb"></a>VB

Si el método se realiza correctamente, el método devuelve S \_ OK.

Si se produce un error en el método , devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

## <a name="remarks"></a>Observaciones

Use este método para seleccionar el nombre del usuario. Una vez seleccionado un nombre de usuario, su valor se puede recuperar llamando al [**método ISCrdEnr::getUserName.**](iscrdenr-getusername.md)

Una alternativa al uso de la interfaz "Seleccionar usuario" es especificar un usuario mediante una llamada al [**método ISCrdEnr::setUserName.**](iscrdenr-setusername.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID ISCrdEnr se define como \_ 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::getUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**ISCrdEnr::resetUser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 




