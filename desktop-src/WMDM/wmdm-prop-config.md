---
title: WMDM_PROP_CONFIG estructura
description: La estructura DE CONFIGURACIÓN DE PROP de WMDM describe un conjunto de valores de propiedad compatibles en todas las propiedades admitidas por el dispositivo \_ \_ para un formato determinado. Esta estructura contiene una serie de descripciones de propiedades en una matriz de estructuras \_ \_ DESC PROP de WMDM.
ms.assetid: cf116861-e31d-4561-b262-e271888afc24
keywords:
- WMDM_PROP_CONFIG estructura windows Media Administrador de dispositivos
topic_type:
- apiref
api_name:
- WMDM_PROP_CONFIG
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e50cd18f5b7646934a6add71674f93ebaae700ab39e57f833e555ea3688ecb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862825"
---
# <a name="wmdm_prop_config-structure"></a>Estructura de configuración \_ de PROP de WMDM \_

La **estructura DE CONFIGURACIÓN DE PROP \_ \_ de WMDM** describe un conjunto de valores de propiedad compatibles en todas las propiedades admitidas por el dispositivo para un formato determinado. Esta estructura contiene una serie de descripciones de propiedades en una matriz de estructuras [**\_ \_ DESC PROP de WMDM.**](wmdm-prop-desc.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WMDM_PROP_CONFIG {
  UINT           nPreference;
  UINT           nPropDesc;
  WMDM_PROP_DESC *pPropDesc;
} WMDM_PROP_CONFIG;
```



## <a name="members"></a>Miembros

<dl> <dt>

**nPreference**
</dt> <dd>

Nivel de preferencia del dispositivo para esta configuración. El valor más bajo indica la configuración más preferida.

</dd> <dt>

**nPropDesc**
</dt> <dd>

Número de descripciones de propiedades contenidas en esta configuración. Hay una sola descripción de propiedad para cada propiedad compatible con el formato especificado.

</dd> <dt>

**pPropDesc**
</dt> <dd>

Puntero a una matriz de [**estructuras \_ \_ DESC PROP de WMDM**](wmdm-prop-desc.md) que contienen descripciones de propiedades. El tamaño de la matriz es igual al valor de **nPropDesc**. La aplicación debe liberar esta memoria cuando haya terminado con ella.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La [**estructura WMDM \_ FORMAT \_ CAPABILITY**](wmdm-format-capability.md) devuelta por [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) para un formato determinado consta de varias configuraciones de propiedades. **WMDM \_ Las \_ estructuras DE CONFIGURACIÓN** DE PROP describen esas configuraciones.

Una configuración de propiedades describe los valores de todas las propiedades admitidas para un formato determinado. Los valores de diferentes propiedades de una sola configuración son compatibles entre sí. Por ejemplo, para un archivo de audio, una configuración incluirá valores válidos de frecuencia de muestreo y valores válidos de la velocidad de bits para que todas las combinaciones de estas velocidades de muestreo y bits se puedan reproducir en el dispositivo.

El autor de la llamada debe liberar la memoria utilizada por **pPropDesc.** Para obtener un ejemplo de cómo hacerlo, vea [**WMDM \_ FORMAT \_ CAPABILITY**](wmdm-format-capability.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**FORMULARIO DE VALORES \_ VÁLIDOS DE \_ PROP DE \_ \_ ENUMERACIÓN WMDM \_**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**FUNCIONALIDAD DE \_ FORMATO \_ WMDM**](wmdm-format-capability.md)
</dt> <dt>

[**WMDM \_ PROP \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**ENUMERACIÓN DE \_ VALORES PROP \_ \_ DE WMDM**](wmdm-prop-values-enum.md)
</dt> <dt>

[**INTERVALO DE VALORES \_ DE PROPIEDAD \_ DE WMDM \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





