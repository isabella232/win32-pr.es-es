---
title: IConfigAsfWriter GetIndexMode, método
description: El método GetIndexMode recupera el modo de índice temporal actual.
ms.assetid: beb874ea-d0d5-4323-a817-47984911da4c
keywords:
- Método GetIndexMode formato de Windows Media
- Método GetIndexMode formato de Windows Media, interfaz IConfigAsfWriter
- Interfaz IConfigAsfWriter formato de Windows Media, método GetIndexMode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb701f591579d3113e79b0b9b74167ac8de3d75f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420969"
---
# <a name="iconfigasfwritergetindexmode-method"></a>IConfigAsfWriter:: GetIndexMode (método)

El método **GetIndexMode** recupera el modo de índice temporal actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIndexMode(
  [out] BOOL *pbIndexFile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbIndexFile* \[ enuncia\]
</dt> <dd>

Puntero a una variable de tipo **bool** que recibe la configuración del modo de índice temporal. Un valor de **true** indica que el escritor ASF de WM está configurado para escribir archivos indizados de forma temporal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si se produce un error, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Utilice este método para determinar si el [escritor ASF de WM](wm-asf-writer-filter.md) está configurado actualmente para escribir archivos ASF indexados temporalmente. Para obtener más información sobre los archivos indizados y indexados de forma temporal, vea los comentarios de [**IConfigAsfWriter:: SetIndexMode**](iconfigasfwriter-setindexmode.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 