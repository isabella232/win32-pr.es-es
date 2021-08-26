---
title: Función MrmCreateConfigInMemory (MrmResourceIndexer.h)
description: Crea nueva información de configuración de PRI inicializada (como datos en memoria, no como un archivo) que define los valores predeterminados del calificador que especifique.
ms.assetid: D8822D6E-5F68-46A1-B99F-52575DB1D277
keywords:
- Menús de la función MrmCreateConfigInMemory y otros recursos
topic_type:
- apiref
api_name:
- MrmCreateConfigInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b30b4a64313952d48662a82e2f62cdef25106136e7757220668fc094c9258d4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011795"
---
# <a name="mrmcreateconfiginmemory-function"></a>Función MrmCreateConfigInMemory

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Crea nueva información de configuración de PRI inicializada (como datos en memoria, no como un archivo) que define los valores predeterminados del calificador que especifique. La función asigna memoria y devuelve un puntero a esa memoria en *outputXmlData.* Llame [**a MrmFreeMemory con**](mrmfreememory.md) el mismo puntero para liberar esa memoria. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de paquetes (PRI) y sistemas [de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmCreateConfigInMemory(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _Out_    BYTE               **outputXmlData,
  _Out_    ULONG              *outputXmlSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*platformVersion* \[ En\]
</dt> <dd>

Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**

La versión de la plataforma *(targetOsVersion)* que se usará para la información de configuración generada.

</dd> <dt>

*defaultQualifiers* \[ en, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Lista de calificadores de recursos predeterminados. Por ejemplo, L"language-en-US \_ scale-100 \_ contrast-standard"

</dd> <dt>

*outputXmlData* \[ out\]
</dt> <dd>

Tipo: **\* \* BYTE**

Dirección de un puntero a BYTE. La función asigna memoria y devuelve un puntero a esa memoria en *outputXmlData.* Llame [**a MrmFreeMemory con**](mrmfreememory.md) el puntero a BYTE para liberar esa memoria.

</dd> <dt>

*outputXmlSize* \[ out\]
</dt> <dd>

Tipo: **ULONG \***

Dirección de un ULONG. En *outputXmlSize*, la función devuelve el tamaño de la memoria asignada a la que *apunta outputXmlData*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

S \_ Ok si la función se ha hecho correctamente; de lo contrario, algún otro valor. Use las macros SUCCEEDED() o FAILED() (definidas en winerror.h) para determinar el éxito o el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de servidor\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

