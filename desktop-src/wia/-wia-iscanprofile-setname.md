---
description: Establece el nombre descriptivo del perfil.
ms.assetid: a0a2de8b-ab7b-49a8-b513-32af0052975f
title: 'IScanProfile:: SetName (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: bd5fbe0e723fea7f7fa75f838b898beceebed0a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716061"
---
# <a name="iscanprofilesetname-method"></a>IScanProfile:: SetName (método)

Establece el nombre descriptivo del perfil.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetName(
  [in] BSTR bstrName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrName* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Nombre descriptivo del perfil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método es necesario porque el GUID de un perfil no se puede usar para mostrar el perfil de digitalización a un usuario.

Un usuario puede cambiar el nombre descriptivo de un perfil con el método [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

Los cambios en un perfil no se guardan en el disco hasta que la aplicación llama al método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .

Si dos aplicaciones crean objetos de Perfil de análisis a partir del mismo archivo XML y cada aplicación escribe cambios en su objeto, solo los cambios realizados por la aplicación que llama a [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last se guardan en el disco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



 

 




