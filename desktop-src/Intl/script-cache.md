---
description: Define una memoria caché de métricas de fuente de Uniscribe.
ms.assetid: 56a98529-6ae9-4b71-bd7d-cf056a1e3683
title: SCRIPT_CACHE (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece29fe0ed610b4576263c36c50311ef57317579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653001"
---
# <a name="script_cache"></a>caché de SCRIPT \_

Define una memoria caché de métricas de fuente de Uniscribe.


```C++
typedef void* SCRIPT_CACHE;
```



## <a name="remarks"></a>Observaciones

Se trata de una estructura opaca. La aplicación debe asignar y conservar una \_ variable de caché de script para cada estilo de carácter utilizado. La variable se debe inicializar en **null**.

Muchas funciones de script toman una combinación de un identificador de contexto de dispositivo de hardware y una variable de caché de SCRIPTs \_ . En primer lugar, se intenta tener acceso a los datos de fuente mediante la variable de caché de SCRIPT \_ . Solo inspecciona el contexto de dispositivo de hardware Si los datos necesarios aún no están almacenados en caché.

El identificador de contexto de dispositivo de hardware se puede pasar a como **null**. Si los datos requeridos por Uniscribe ya están almacenados en caché, no se tiene acceso al contexto del dispositivo y la operación continúa con normalidad.

Si el contexto del dispositivo se pasa como **null** y Uniscribe tiene que tener acceso a él por cualquier motivo, Uniscribe devuelve el código de error E \_ pendiente. Este código se devuelve rápidamente, lo que permite que la aplicación evite las llamadas [**SeleccionarObjeto**](/windows/win32/api/wingdi/nf-wingdi-selectobject) que consumen mucho tiempo.

## <a name="examples"></a>Ejemplos

El ejemplo siguiente se aplica a todas las funciones que toman una variable de caché de SCRIPTs \_ y un identificador opcional para un contexto de dispositivo de hardware.


```C++
hr = ScriptShape(NULL, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
if (hr == E_PENDING)
{
    // ... select font into hdc ...
    hr = ScriptShape(hdc, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Estructuras de Uniscribe](uniscribe-structures.md)
</dt> <dt>

[Almacenamiento en caché](caching.md)
</dt> </dl>

 

 
