---
title: DRM_LICENSE_STATE_DATA estructura (wmdrmsdk. h)
description: La \_ \_ \_ estructura de datos de estado de la licencia DRM contiene información sobre las restricciones de licencia de un derecho DRM.
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- DRM_LICENSE_STATE_DATA estructura de Windows Media Format
- Formato de Windows Media de estructura
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
ms.openlocfilehash: b02f38b8f09b7b444949e9477635e6b8770fc168
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709038"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a>DRM_LICENSE_STATE_DATA estructura (wmdrmsdk. h)

La estructura de datos de estado de la **\_ licencia \_ \_ DRM** contiene información sobre las restricciones de licencia de un derecho DRM.

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

Categoría de cadena que se va a mostrar. Consulte [**\_ categoría de \_ estado \_ de licencia de DRM**](drmdrm-license-state-category.md) para ver los valores posibles y su significado.

</dd> <dt>

**dwNumCounts**
</dt> <dd>

Número de elementos proporcionados en **dwCount**. Normalmente, este valor es 0 o 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Matriz de 0 ó 1 o más valores **DWORD** que representan el número de veces que se puede realizar la acción especificada en **dwCategory** . Vea la sección Comentarios.

</dd> <dt>

**dwNumDates**
</dt> <dd>

Número de elementos proporcionados en **fecha y hora**. Normalmente no se usan más de dos fechas, por ejemplo, con una licencia válida de una fecha hasta otra.

</dd> <dt>

**fecha y hora \[ 4\]**
</dt> <dd>

Una matriz de una o varias estructuras **FILETIME** que representan una o más fechas de la licencia. El significado de una fecha determinada depende del valor de **dwCategory**.

</dd> <dt>

**dwVague**
</dt> <dd>

Cero o más de los siguientes marcadores combinados con **una operación OR** bit a bit:



| Marca                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| datos de estado de licencia de DRM \_ \_ \_ \_ imprecisos        | Si se establece, puede haber más licencias que se apliquen al contenido. La única manera de estar seguro de las licencias individuales que se aplican a un identificador de clave determinado es enumerar las licencias. Para ello, llame a [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), pasando el identificador de clave como parámetro bstrKID. A continuación, use la interfaz IWMDRMLicense recuperada para examinar las licencias. |
| Estado de la licencia de DRM \_ \_ datos de \_ \_ OPL \_ presente | Si se establece, la licencia incluye los niveles de protección de salida (OPLs) que deben recuperarse y comprobarse con el destino de la salida de la aplicación.                                                                                                                                                                                                                                                                                  |
| datos de estado de licencia de DRM \_ \_ \_ \_ SAP \_ presentes | Si se establece, el contenido se debe entregar mediante la ruta de acceso de audio segura (SAP).                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se recupera llamando a **IWMDRMLicenseQuery:: QueryLicenseState**.

Si **dwCategory** es **el \_ \_ \_ \_ recuento de Estados \_ de licencias de DRM de WM desde \_ hasta**, la matriz de **DateTime** normalmente contendrá dos fechas: una fecha "desde" y una fecha "hasta". También se pueden especificar dos pares de fecha para crear licencias más complejas.

Los elementos de la matriz **dwCount** se corresponden con las fechas o intervalos de fechas especificados en la matriz **DateTime** . Si **dwCategory** es **el \_ \_ \_ \_ recuento de Estados \_ de licencias de DRM de WM desde \_ hasta** y **fecha y hora** contiene un par de fechas, **dwCount** contendrá un elemento. Si **DateTime** contiene dos pares de fecha (cuatro elementos), **dwCount** debe contener dos elementos, uno para cada par de fechas.

En algunos casos, es posible que los usuarios hayan emitido más de una licencia para un archivo. Por ejemplo, podrían haber adquirido una licencia que permitía cinco jugadas hasta el final del mes y, posteriormente, adquirió una segunda licencia para derechos ilimitados. En tal caso, la marca de \_ datos de estado de la licencia DRM \_ \_ \_ se establece en **dwVague** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ) y el componente DRM usará un algoritmo para determinar el conjunto de derechos más probable que se haya aplicado. Cuando expire una licencia, el componente DRM examinará las licencias restantes y así sucesivamente hasta que hayan expirado todas las licencias.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





