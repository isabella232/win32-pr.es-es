---
title: Función MrmCreateConfigInMemory (MrmResourceIndexer. h)
description: Crea una nueva información de configuración de PRI inicializada (como datos en memoria, no como un archivo) que define los valores predeterminados del calificador que especifique.
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
ms.openlocfilehash: 0d809ac640061ecf8bd51b9e2016aefe537b1ee8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535080"
---
# <a name="mrmcreateconfiginmemory-function"></a>MrmCreateConfigInMemory función)

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Crea una nueva información de configuración de PRI inicializada (como datos en memoria, no como un archivo) que define los valores predeterminados del calificador que especifique. La función asigna memoria y devuelve un puntero a esa memoria en *outputXmlData*. Llame a [**MrmFreeMemory**](mrmfreememory.md) con el mismo puntero para liberar esa memoria. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

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

*platformVersion* \[ de\]
</dt> <dd>

Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**

Versión de la plataforma (*targetOsVersion*) que se va a usar para la información de configuración generada.

</dd> <dt>

*defaultQualifiers* \[ en, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Una lista de calificadores de recursos predeterminados. Por ejemplo, L "Language-en-US \_ Scale-100 \_ Contrast-Standard"

</dd> <dt>

*outputXmlData* \[ enuncia\]
</dt> <dd>

Tipo: **byte \* \***

Dirección de un puntero a BYTE. La función asigna memoria y devuelve un puntero a esa memoria en *outputXmlData*. Llame a [**MrmFreeMemory**](mrmfreememory.md) con el puntero en byte para liberar esa memoria.

</dd> <dt>

*outputXmlSize* \[ enuncia\]
</dt> <dd>

Tipo: **ULong \** _

Dirección de un ULONG. En _outputXmlSize *, la función devuelve el tamaño de la memoria asignada a la que apunta *outputXmlData*.

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

 

