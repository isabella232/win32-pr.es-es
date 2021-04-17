---
description: Enumera el nombre de los proveedores de servicios de cifrado (CSP) disponibles.
ms.assetid: d0dc8a8a-afff-4ccc-96e0-2c52913c3322
title: 'ISCrdEnr:: enumCSPName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCSPName
- SCrdEnr.enumCSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e7bba587b56300cd02efd81758288d3b77c65a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546683"
---
# <a name="iscrdenrenumcspname-method"></a>ISCrdEnr:: enumCSPName (método)

El método **enumCSPName** enumera el nombre de los proveedores de [*servicios de cifrado*](../secgloss/c-gly.md) (CSP) disponibles.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT enumCSPName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCSPName
);
```


```VB

SCrdEnr.enumCSPName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCSPName _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwIndex* \[ de\]
</dt> <dd>

Índice de base cero de la secuencia de enumeración.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Reservado para uso futuro. Establezca este valor en cero.

</dd> <dt>

*pbstrCSPName* \[ enuncia\]
</dt> <dd>

Puntero a una cadena que devuelve el nombre del CSP enumerado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

### <a name="vb"></a>VB

Cadena que representa el nombre del CSP enumerado.

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

[**ISCrdEnr::CSPCount**](iscrdenr-cspcount.md)
</dt> <dt>

[**ISCrdEnr::CSPName**](iscrdenr-cspname.md)
</dt> </dl>

 

 
