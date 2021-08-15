---
title: DRM_LICENSE_STATE_DATA estructura (Drternals.h)
description: La estructura \_ DRM LICENSE STATE DATA contiene información de licencia sobre un derecho DRM \_ \_ especificado.
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- DRM_LICENSE_STATE_DATA windows Media Format de estructura
- estructura windows Formato multimedia
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6703481dc1d3608a8bf08ab2bbd216db4a9ecdc91bd4604d2b9de7d7de4fa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848538"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a>DRM_LICENSE_STATE_DATA estructura (Drternals.h)

La **estructura DRM LICENSE STATE \_ \_ \_ DATA** contiene [*información de*](wmformat-glossary.md) licencia sobre un derecho [*DRM*](wmformat-glossary.md) especificado.

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

Categoría de cadena que se va a mostrar. Consulte [**DRM LICENSE STATE CATEGORY \_ \_ \_ (CATEGORÍA DE ESTADO DE LICENCIA**](drm-license-state-category.md) DE DRM) para ver los valores posibles y su significado.

</dd> <dt>

**dwNumCounts**
</dt> <dd>

Número de elementos proporcionados en **dwCount**. Este valor suele ser 0 o 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Matriz de 0 o 1 o más **DWORD** que representan el número de veces que se puede realizar la acción especificada en **dwCategory.** Vea Notas.

</dd> <dt>

**dwNumDates**
</dt> <dd>

Número de elementos proporcionados en **datetime.** Normalmente no se usan más de dos fechas, por ejemplo, con una licencia válida desde una fecha hasta otra.

</dd> <dt>

**datetime \[ 4\]**
</dt> <dd>

Matriz de una o varias estructuras FILETIME que representan una o varias fechas de la licencia. El significado de una fecha determinada depende del valor de **dwCategory**.

</dd> <dt>

**dwVague**
</dt> <dd>

Cero o más de las marcas siguientes combinadas con un OR bit a **bit:**



| Marca                                    | Descripción                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| DRM \_ LICENSE STATE DATA \_ \_ \_ IMPRECISO        | Si se establece, puede haber más licencias que se apliquen al contenido.                                                                                         |
| OPL \_ DE DATOS DE ESTADO DE LICENCIA DRM \_ \_ \_ \_ PRESENTE | Si se establece, la licencia incluye los niveles de protección de salida (OPL) que se deben recuperar y comprobar en el destino de la salida de la aplicación. |
| DRM \_ LICENSE \_ STATE \_ DATA \_ SAP \_ PRESENT | Si se establece, el contenido debe entregarse mediante la ruta de acceso de audio segura (SAP).                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se devuelve (encapsulada en una estructura [**WM \_ LICENSE STATE \_ \_ DATA)**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) desde una llamada a [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) cuando se especifica una de las propiedades de estado de licencia de DRM. Estas propiedades son:

-   [**DRM \_ LicenseState \_ Playback**](drm-licensestate-playback.md)
-   [**DRM \_ LicenseState \_ CopyToCD**](drm-licensestate-copytocd.md)
-   [**DRM \_ LicenseState \_ CopyToSDMIDevice**](drm-licensestate-copytosdmidevice.md)
-   [**DRM \_ LicenseState \_ CopyToNonSDMIDevice**](drm-licensestate-copytononsdmidevice.md)
-   [**DRM \_ LicenseState \_ CollaborativePlay**](drm-licensestate-collaborativeplay.md)
-   [**Copia \_ de LicenseState de DRM \_**](drm-licensestate-copy.md)
-   [**Lista \_ de reproducción de DRM LicenseState \_**](drm-licensestate-playlistburn.md)

Si **dwCategory** es **WM DRM LICENSE STATE COUNT FROM \_ \_ \_ \_ \_ \_ UNTIL,** la matriz **datetime** normalmente contendrá dos fechas, una fecha "from" y una fecha "until". También se pueden especificar dos pares de fechas para crear licencias más complejas.

Los elementos de la **matriz dwCount** corresponden a las fechas o intervalos de fechas especificados en la **matriz datetime.** Si **dwCategory** es **WM DRM LICENSE STATE COUNT FROM \_ \_ \_ \_ \_ \_ UNTIL** y **datetime** contiene un par de fechas, **dwCount** contendrá un elemento. Si **datetime contiene** dos pares de fecha (cuatro elementos), **dwCount** debe contener dos elementos, uno para cada par de fechas.

En algunos casos, es posible que a los usuarios se le haya emitido más de una licencia para un archivo. Por ejemplo, podrían haber adquirido una licencia que permitió cinco juegos hasta el final del mes y, posteriormente, adquirir una segunda licencia para derechos ilimitados. En tal caso, la marca DRM LICENSE STATE DATA ALGORITHM se establece en \_ \_ \_ \_ **dwVague** ( ) y el componente DRM usará un algoritmo para determinar el conjunto más probable de derechos que se han `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` aplicado. Cuando una licencia expira, el componente DRM examinará las licencias restantes, y así sucesivamente hasta que todas las licencias expiren.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                      |
| Versión<br/>                  | Windows SDK de formato multimedia 7 o versiones posteriores del SDK<br/>                       |
| Header<br/>                   | <dl> <dt>Drternals.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

