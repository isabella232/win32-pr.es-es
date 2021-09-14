---
description: Determina si una configuración regional especificada por nombre está instalada o se admite en el sistema operativo.
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: Función RtlIsValidLocaleName (Ntrtl.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171945"
---
# <a name="rtlisvalidlocalename-function"></a>Función RtlIsValidLocaleName

Determina si una configuración regional especificada por nombre está instalada o se admite en el sistema operativo.

> [!Note]  
> Esta función solo está disponible para su uso Windows Vista. Podría modificarse o no estar disponible en versiones posteriores. Las aplicaciones deben [**usar IsValidLocaleName.**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LocaleName* \[ En\]
</dt> <dd>

[Nombre de configuración regional que se](locale-names.md) validará. Este parámetro puede especificar el nombre de una [configuración regional personalizada.](custom-locales.md)

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Marcas que indican si las configuraciones regionales neutras se consideran válidas. Actualmente, la única marca definida es [LOCALE \_ ALLOW \_ NEUTRAL.](locale-allow-neutral.md) El valor predeterminado es que no lo están.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o 0 en caso contrario.

## <a name="remarks"></a>Observaciones

Esta función es similar a [**IsValidLocaleName.**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) La única diferencia es que si se establece LOCALE \_ ALLOW \_ NEUTRAL, **RtlIsValidLocaleName** devuelve **TRUE** para un nombre que corresponde a una configuración regional neutra (como "en"), mientras [**que IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) devuelve **TRUE** solo para una configuración regional específica (como "en-US"). Las configuraciones regionales neutras se usan como parte de la estrategia de carga de recursos en Windows Vista y versiones posteriores. Solo una pequeña clase de aplicaciones altamente especializadas usa **RtlIsValidLocaleName** y establece LOCALE ALLOW NEUTRAL, ya que las configuraciones regionales neutras tienen \_ un uso muy \_ limitado. Ninguna de las funciones descritas en [Llamar a las funciones "Nombre de configuración regional"](calling-the--locale-name--functions.md) acepta configuraciones regionales neutras como entradas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Ntrtl.h</dt> </dl>      |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Compatibilidad con idiomas nacionales](national-language-support.md)
</dt> <dt>

[Funciones de compatibilidad con idiomas nacionales](national-language-support-functions.md)
</dt> <dt>

[**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




