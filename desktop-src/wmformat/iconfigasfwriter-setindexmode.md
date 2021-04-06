---
title: IConfigAsfWriter SetIndexMode, método
description: El método SetIndexMode permite que la aplicación controle si el archivo se indizará temporalmente.
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- Método SetIndexMode formato de Windows Media
- Método SetIndexMode formato de Windows Media, interfaz IConfigAsfWriter
- Interfaz IConfigAsfWriter formato de Windows Media, método SetIndexMode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25d5f2b985aeca490323aecaef2595d52b99056c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077798"
---
# <a name="iconfigasfwritersetindexmode-method"></a>IConfigAsfWriter:: SetIndexMode (método)

El método **SetIndexMode** permite que la aplicación controle si el archivo se indizará temporalmente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bIndexFile* \[ de\]
</dt> <dd>

Variable de tipo **bool**; **True** especifica que el archivo se indexará temporalmente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si se produce un error, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

De forma predeterminada, el [escritor ASF de WM](wm-asf-writer-filter.md) crea archivos ASF indexados temporalmente. Realiza la indexación cuando se detiene el gráfico. Puede deshabilitar este comportamiento si desea realizar su propia indexación basada en marco como paso posterior al procesamiento. Para crear un archivo indexado por fotogramas, llame a **SetIndexMode**(false), cree el archivo y, a continuación, use los métodos del SDK de Windows Media Format directamente para crear un índice basado en marco para el archivo.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 