---
title: DRM_LICENSE_STATE_DATA estructura (Wmdrmsdk.h)
description: La estructura DRM \_ LICENSE STATE DATA contiene información sobre las \_ \_ restricciones de licencia de un derecho DRM.
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- DRM_LICENSE_STATE_DATA structure windows Media Format
- Estructura de windows Formato multimedia
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63ba00384ec7c3340aa099f1b427cd8953969704bd0585f0da58cd4fd0ffd6ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708935"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a>DRM_LICENSE_STATE_DATA estructura (Wmdrmsdk.h)

La **estructura DRM LICENSE STATE \_ \_ \_ DATA** contiene información sobre las restricciones de licencia de un derecho DRM.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_LICENSE_STATE_DATA {
  DWORD                      dwStreamId;
  DRM_LICENSE_STATE_CATEGORY dwCategory;
  DWORD                      dwNumCounts;
  DWORD                      dwCount[4];
  DWORD                      dwNumDates;
  FILETIME                   datetime[4];
  DWORD                      dwVague;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwStreamId**
</dt> <dd>

Número de secuencia al que se aplica la licencia. Debe ser 0, lo que indica que la licencia se aplica a todas las secuencias del archivo.

</dd> <dt>

**dwCategory**
</dt> <dd>

Categoría de cadena que se va a mostrar. Consulte [**DRM LICENSE STATE CATEGORY \_ \_ \_ (CATEGORÍA DE ESTADO DE LICENCIA DE DRM)**](drmdrm-license-state-category.md) para ver los valores posibles y su significado.

</dd> <dt>

**dwNumCounts**
</dt> <dd>

Número de elementos proporcionados en **dwCount**. Este valor suele ser 0 o 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Matriz de 0 o 1 o más valores **DWORD** que representan el número de veces que se puede realizar la acción especificada en **dwCategory.** Vea la sección Comentarios.

</dd> <dt>

**dwNumDates**
</dt> <dd>

Número de elementos proporcionados en **datetime.** Normalmente no se usan más de dos fechas, por ejemplo, con una licencia válida desde una fecha hasta otra.

</dd> <dt>

**datetime \[ 4\]**
</dt> <dd>

Matriz de una o varias estructuras **FILETIME** que representan una o varias fechas de la licencia. El significado de una fecha determinada depende del valor de **dwCategory**.

</dd> <dt>

**dwVague**
</dt> <dd>

Cero o más de las marcas siguientes combinadas con un OR bit a **bit:**



| Marca                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMPRECISO \_ DE DATOS DE ESTADO DE LICENCIA \_ \_ \_ DRM        | Si se establece, puede haber más licencias que se apliquen al contenido. La única manera de estar seguro sobre las licencias individuales que se aplican a un identificador de clave determinado es enumerar las licencias. Para ello, llame a [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)y pase el identificador de clave como parámetro bstrKID. A continuación, use la interfaz IWMDRMLicense recuperada para examinar las licencias. |
| OPL \_ DE DATOS DE ESTADO DE LICENCIA DRM \_ \_ \_ \_ PRESENTE | Si se establece, la licencia incluye los niveles de protección de salida (OPL) que se deben recuperar y comprobar con el destino de la salida de la aplicación.                                                                                                                                                                                                                                                                                  |
| PRESENTE SAP \_ DE DATOS DE ESTADO DE LICENCIA \_ \_ \_ \_ DRM | Si se establece, el contenido debe entregarse mediante la ruta de acceso de audio segura (SAP).                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se recupera mediante una llamada **a IWMDRMLicenseQuery::QueryLicenseState**.

Si **dwCategory** es **WM DRM LICENSE STATE COUNT FROM \_ \_ \_ \_ \_ \_ UNTIL**, la matriz **datetime** normalmente contendrá dos fechas: una fecha "from" y una fecha "until". También se pueden especificar dos pares de fechas para crear licencias más complejas.

Los elementos de la **matriz dwCount** corresponden a las fechas o intervalos de fechas especificados en la **matriz datetime.** Si **dwCategory** es **WM DRM LICENSE STATE COUNT FROM \_ \_ \_ \_ \_ \_ UNTIL** y **datetime** contiene un par de fechas, **dwCount** contendrá un elemento. Si **datetime contiene** dos pares de fechas (cuatro elementos), **dwCount** debe contener dos elementos, uno para cada par de fechas.

En algunos casos, es posible que los usuarios hayan emitido más de una licencia para un archivo. Por ejemplo, podrían haber adquirido una licencia que permitió cinco juegos hasta el final del mes y, posteriormente, haber adquirido una segunda licencia para derechos ilimitados. En tal caso, la marca DRM LICENSE STATE DATA VAGUE se establece en \_ \_ \_ \_ **dwVague** ( ) y el componente DRM usará un algoritmo para determinar el conjunto más probable de derechos que se han `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` aplicado. Cuando expira una licencia, el componente DRM examinará las licencias restantes, y así sucesivamente hasta que todas las licencias expiren.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





