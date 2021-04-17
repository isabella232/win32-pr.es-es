---
title: Función MrmFreeMemory (MrmResourceIndexer. h)
description: Libera memoria asignada por MrmCreateConfigInMemory, MrmCreateResourceFileInMemory, MrmDumpPriFileInMemory y MrmDumpPriDataInMemory.
ms.assetid: F8741379-CE1A-47BD-9B2C-721A5424CAD1
keywords:
- Menús de la función MrmFreeMemory y otros recursos
topic_type:
- apiref
api_name:
- MrmFreeMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c255cb4d1c73e40b5636914d2bc70ae4e1efe3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666053"
---
# <a name="mrmfreememory-function"></a>MrmFreeMemory función)

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Libera memoria asignada por [**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)y [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md). Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmFreeMemory(
  _In_ BYTE *data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*datos* \[ de de\]
</dt> <dd>

Tipo: **byte \** _

Puntero a la memoria asignada y devuelta por [_ *MrmCreateConfigInMemory* *](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)o [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor. Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server \[\]<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mrmsupport. lib</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

