---
title: DRM_LICENSE_STATE_DATA estructura (Drmexternals. h)
description: La estructura de datos de estado de la \_ licencia DRM \_ \_ contiene información de licencia sobre un derecho DRM especificado.
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- DRM_LICENSE_STATE_DATA estructura de Windows Media Format
- Formato de Windows Media de estructura
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
ms.openlocfilehash: 3bb63bce02a52aefcf1f3351fe34ab008996aa0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705161"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a>DRM_LICENSE_STATE_DATA estructura (Drmexternals. h)

La estructura de datos de estado de la **\_ licencia \_ \_ DRM** contiene información de [*licencia*](wmformat-glossary.md) sobre un derecho [*DRM*](wmformat-glossary.md) especificado.

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

Categoría de cadena que se va a mostrar. Consulte [**\_ categoría de \_ estado \_ de licencia de DRM**](drm-license-state-category.md) para ver los valores posibles y su significado.

</dd> <dt>

**dwNumCounts**
</dt> <dd>

Número de elementos proporcionados en **dwCount**. Normalmente, este valor es 0 o 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Una matriz de 0 o 1 o más **DWORD** s que representan el número de veces que se puede realizar la acción especificada en **dwCategory** . Vea Notas.

</dd> <dt>

**dwNumDates**
</dt> <dd>

Número de elementos proporcionados en **fecha y hora**. Normalmente no se usan más de dos fechas, por ejemplo, con una licencia válida de una fecha hasta otra.

</dd> <dt>

**fecha y hora \[ 4\]**
</dt> <dd>

Una matriz de una o varias estructuras FILETIME que representan una o más fechas de la licencia. El significado de una fecha determinada depende del valor de **dwCategory**.

</dd> <dt>

**dwVague**
</dt> <dd>

Cero o más de los siguientes marcadores combinados con **una operación OR** bit a bit:



| Marca                                    | Descripción                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| datos de estado de licencia de DRM \_ \_ \_ \_ imprecisos        | Si se establece, puede haber más licencias que se apliquen al contenido.                                                                                         |
| Estado de la licencia de DRM \_ \_ datos de \_ \_ OPL \_ presente | Si se establece, la licencia incluye los niveles de protección de salida (OPLs) que deben recuperarse y comprobarse con el destino de la salida de la aplicación. |
| datos de estado de licencia de DRM \_ \_ \_ \_ SAP \_ presentes | Si se establece, el contenido se debe entregar mediante la ruta de acceso de audio segura (SAP).                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se devuelve (encapsulada en una estructura de [**\_ datos de \_ estado \_**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) de la licencia de WM) de una llamada a [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) cuando se especifica una de las propiedades de estado de licencia de DRM. Estas propiedades son:

-   [**\_Reproducción de LICENSESTATE DRM \_**](drm-licensestate-playback.md)
-   [**\_CopyToCD LICENSESTATE \_ DRM**](drm-licensestate-copytocd.md)
-   [**\_CopyToSDMIDevice LICENSESTATE \_ DRM**](drm-licensestate-copytosdmidevice.md)
-   [**\_CopyToNonSDMIDevice LICENSESTATE \_ DRM**](drm-licensestate-copytononsdmidevice.md)
-   [**\_CollaborativePlay LICENSESTATE \_ DRM**](drm-licensestate-collaborativeplay.md)
-   [**\_Copia de LicenseState de DRM \_**](drm-licensestate-copy.md)
-   [**\_PlaylistBurn LICENSESTATE \_ DRM**](drm-licensestate-playlistburn.md)

Si **dwCategory** es **el \_ \_ \_ \_ recuento de Estados \_ de licencias de DRM de WM desde \_ hasta,** la matriz de **DateTime** normalmente contendrá dos fechas, una fecha "desde" y una fecha "hasta". También se pueden especificar dos pares de fecha para crear licencias más complejas.

Los elementos de la matriz **dwCount** se corresponden con las fechas o intervalos de fechas especificados en la matriz **DateTime** . Si **dwCategory** es **el \_ \_ \_ \_ recuento de Estados \_ de licencias de DRM de WM desde \_ hasta** y **fecha y hora** contiene un par de fechas, **dwCount** contendrá un elemento. Si **DateTime** contiene dos pares de fecha (cuatro elementos), **dwCount** debe contener dos elementos, uno para cada par de fechas.

En algunos casos, es posible que los usuarios hayan emitido más de una licencia para un archivo. Por ejemplo, podrían haber adquirido una licencia que permitía cinco jugadas hasta el final del mes y, posteriormente, adquirió una segunda licencia para derechos ilimitados. En tal caso, la marca de \_ datos de estado de la licencia DRM \_ \_ \_ se establece en **dwVague** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ) y el componente DRM usará un algoritmo para determinar el conjunto de derechos más probable que se haya aplicado. Cuando expire una licencia, el componente DRM examinará las licencias restantes y así sucesivamente hasta que hayan expirado todas las licencias.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                      |
| Versión<br/>                  | SDK de Windows Media Format 7 o versiones posteriores del SDK<br/>                       |
| Encabezado<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

