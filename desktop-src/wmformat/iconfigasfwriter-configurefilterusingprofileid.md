---
title: IConfigAsfWriter ConfigureFilterUsingProfileId, método
description: El método ConfigureFilterUsingProfileId configura el filtro para escribir un archivo ASF con un índice de identificador de perfil (ID.) de la lista de perfiles del sistema. (Solo para perfiles de Windows Media Format 4,0).
ms.assetid: b0375785-83db-4540-aca9-7ba0bb81c1ef
keywords:
- Método ConfigureFilterUsingProfileId formato de Windows Media
- Método ConfigureFilterUsingProfileId formato de Windows Media, interfaz IConfigAsfWriter
- Interfaz IConfigAsfWriter formato de Windows Media, método ConfigureFilterUsingProfileId
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0226195d7657667e3947b55546b321edafa7befc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714398"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a>IConfigAsfWriter:: ConfigureFilterUsingProfileId (método)

El método **ConfigureFilterUsingProfileId** configura el filtro para escribir un archivo ASF con un índice de identificador de perfil (ID.) de la lista de perfiles del sistema. (Solo para perfiles de Windows Media Format 4,0).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConfigureFilterUsingProfileId(
  [in] DWORD dwProfileId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwProfileId* \[ de\]
</dt> <dd>

IDENTIFICADOR de perfil tal y como se define en la versión 4,0 del SDK de Windows Media Format.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** .



| Código devuelto                                                                                         | Descripción                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                | El método se ha llevado a cabo de forma correcta.<br/>        |
| <dl> <dt>**E \_ FAIL**</dt> </dl>              | El perfil no es válido.<br/>    |
| <dl> <dt>**Estado de VFW \_ E \_ incorrecto \_**</dt> </dl> | El gráfico de filtro está detenido.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método está ahora obsoleto porque supone la versión 4,0 perfiles de SDK de Windows Media Format. Para configurar el filtro para la versión 7,0 y los perfiles posteriores, use [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) o [**IConfigAsfWriter:: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

