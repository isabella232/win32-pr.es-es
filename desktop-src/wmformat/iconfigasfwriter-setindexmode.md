---
title: Método IConfigAsfWriter SetIndexMode
description: El método SetIndexMode permite a la aplicación controlar si el archivo se indexa temporalmente.
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- Formato multimedia de windows del método SetIndexMode
- Método SetIndexMode windows Media Format, interfaz IConfigAsfWriter
- IConfigAsfWriter interface windows Media Format , SetIndexMode (método)
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b65fbd3d279b8a66c132d24476b09b0f897c5993ea9a97d86096cf856832f9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433632"
---
# <a name="iconfigasfwritersetindexmode-method"></a>IConfigAsfWriter::SetIndexMode (método)

El **método SetIndexMode** permite a la aplicación controlar si el archivo se indexa temporalmente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bIndexFile* \[ En\]
</dt> <dd>

Variable de tipo **BOOL**; **TRUE** especifica que el archivo se indexará temporalmente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve S \_ OK. Si se produce un error, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

De forma predeterminada, [WM ASF Writer](wm-asf-writer-filter.md) crea archivos ASF indexados temporalmente. Realiza la indexación cuando se detiene el gráfico. Puede deshabilitar este comportamiento si desea realizar su propia indexación basada en fotogramas como paso posterior al procesamiento. Para crear un archivo indexado por fotogramas, llame a **SetIndexMode**(FALSE), cree el archivo y, a continuación, use los métodos del SDK de formato multimedia de Windows directamente para crear un índice basado en fotogramas para el archivo.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConfigAsfWriter (Interfaz)**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 