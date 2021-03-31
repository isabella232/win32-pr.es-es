---
description: Determina si una configuración regional especificada por nombre se instala o se admite en el sistema operativo.
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: Función RtlIsValidLocaleName (Ntrtl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsValidLocaleName
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 3433daaf48e81f662945f1d223e9cf7188ddb706
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907892"
---
# <a name="rtlisvalidlocalename-function"></a>RtlIsValidLocaleName función)

Determina si una configuración regional especificada por nombre se instala o se admite en el sistema operativo.

> [!Note]  
> Esta función solo está disponible para su uso en Windows Vista. Podría modificarse o no estar disponible en versiones posteriores. Las aplicaciones deben usar [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LocaleName* \[ de\]
</dt> <dd>

[Nombre de la configuración regional](locale-names.md) que se va a validar. Este parámetro puede especificar el nombre de una [configuración regional personalizada](custom-locales.md).

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Marcas que indican si las configuraciones regionales neutras se consideran válidas. Actualmente, la única marca definida es [ \_ permitir la \_ configuración regional](locale-allow-neutral.md). El valor predeterminado es que no son.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o 0 en caso contrario.

## <a name="remarks"></a>Observaciones

Esta función es similar a [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename). La única diferencia es que si se establece la configuración regional \_ Allow \_ neutral, **RtlIsValidLocaleName** devuelve **true** para un nombre que se corresponde con una configuración regional neutra (como "en"), mientras que [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) solo devuelve **true** para una configuración regional concreta (como "en-US"). Las configuraciones regionales neutras se utilizan como parte de la estrategia de carga de recursos en Windows Vista y versiones posteriores. Solo una pequeña clase de aplicaciones muy especializadas usa **RtlIsValidLocaleName** y establece la configuración regional para \_ que \_ sea neutra, ya que las configuraciones regionales neutras son de uso muy limitado. Ninguna de las funciones descritas en [llamada a las funciones de "nombre de configuración regional"](calling-the--locale-name--functions.md) acepta configuraciones regionales neutras como entradas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Ntrtl. h</dt> </dl>      |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con National Language](national-language-support.md)
</dt> <dt>

[Funciones de soporte de National Language](national-language-support-functions.md)
</dt> <dt>

[**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




