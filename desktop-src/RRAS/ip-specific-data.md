---
title: Estructura de IP_SPECIFIC_DATA (RTM. h)
description: La \_ estructura de datos específica de IP contiene datos específicos de IP.
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- IP_SPECIFIC_DATA de la estructura RAS
- PIP_SPECIFIC_DATA de puntero de estructura RAS
topic_type:
- apiref
api_name:
- IP_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a3ed319f7cf42295bf918ed3ec67f5d59fe5d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150618"
---
# <a name="ip_specific_data-structure"></a>\_Estructura de datos específica de IP \_

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La estructura de **\_ datos específica de IP** contiene datos específicos de IP.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _IP_SPECIFIC_DATA {
  DWORD FSD_Type;
  DWORD FSD_Policy;
  DWORD FSD_NextHopAS;
  DWORD FSD_Priority;
  DWORD FSD_Metric;
  DWORD FSD_Metric1;
  DWORD FSD_Metric2;
  DWORD FSD_Metric3;
  DWORD FSD_Metric4;
  DWORD FSD_Metric5;
  DWORD FSD_Flags;
} IP_SPECIFIC_DATA, *PIP_SPECIFIC_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Tipo FSD**
</dt> <dd>

Especifica el tipo de ruta tal y como se define en [RFC 1354](routing-protocols-request-for-comments.md). En la tabla siguiente se muestran los valores posibles para este miembro.



| Miembro                                                                                               | Significado                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | No se ha especificado el tipo de ruta. El tipo es diferente del que se muestra aquí.<br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | La ruta no es válida. Normalmente, este valor se usa para invalidar una ruta. Sin embargo, dado que el administrador de tablas de enrutamiento no admite la invalidación, la ruta se sigue considerando en los cálculos de la mejor ruta. Por lo tanto, los protocolos de enrutamiento no deben usar este valor.<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | La ruta es una ruta local, es decir, el próximo salto es el destino final.<br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | La ruta es una ruta remota, es decir, el próximo salto no es el destino final.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**\_Directiva FSD**
</dt> <dd>

Especifica el conjunto de condiciones que daría lugar a la selección de una ruta de múltiples rutas. Este miembro está normalmente en formato TOS de IP. Para obtener más información, consulte [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ NextHopAS**
</dt> <dd>

Especifica el número de sistema autónomo del próximo salto.

</dd> <dt>

**Prioridad de FSD \_**
</dt> <dd>

Especifica un valor de métrica. El administrador de tablas de enrutamiento usa este valor para comparar esta entrada de ruta con las entradas de ruta obtenidas de otros protocolos de enrutamiento. El valor de este miembro se establece mediante el administrador de tablas de enrutamiento.

</dd> <dt>

**Métrica de FSD \_**
</dt> <dd>

Especifica un valor de métrica. El administrador de tablas de enrutamiento usa este valor para comparar esta entrada de ruta con otras entradas de ruta obtenidas del mismo protocolo de enrutamiento. El valor de este miembro se establece mediante el protocolo de enrutamiento.

</dd> <dt>

**FSD \_ Metric1**
</dt> <dd>

Especifica un valor de métrica específico del Protocolo de enrutamiento. Este valor de métrica se documenta en [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ métrica2**
</dt> <dd>

Especifica un valor de métrica específico del Protocolo de enrutamiento. Este valor de métrica se documenta en [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ Metric3**
</dt> <dd>

Especifica un valor de métrica específico del Protocolo de enrutamiento. Este valor de métrica se documenta en [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ Metric4**
</dt> <dd>

Especifica un valor de métrica específico del Protocolo de enrutamiento. Este valor de métrica se documenta en [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ Metric5**
</dt> <dd>

Especifica un valor de métrica específico del Protocolo de enrutamiento. Este valor de métrica se documenta en [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**Marcas de FSD \_**
</dt> <dd>

Especifica si la ruta es válida. El protocolo de enrutamiento debe borrar primero estas marcas y, a continuación, establecer la ruta como válida o no válida. El protocolo de enrutamiento debe usar las macros **ClearRouteFlags ()**, **SetRouteValid ()** y **ClearRouteValid ()** para realizar estas operaciones. Estas macros se definen en RTM. h.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El administrador de tablas de enrutamiento usa los miembros **FSD \_ Priority** y **FSD \_ Metric** para calcular la mejor ruta a una red de destino determinada.

Los **miembros \_ \[ 1-5 \]** de la métrica de FSD son para la conformidad con la MIB II. Los agentes MIB II solo muestran estos valores de métrica. No muestran el valor de **métrica \_ FSD** . Para que se muestre la **\_ métrica FSD** , el protocolo de enrutamiento también debe almacenar el valor en uno de los miembros **FSD \_ Metric \[ 1-5 \]** .

El administrador de tablas de enrutamiento no usa los valores de métricas de los miembros de la **métrica de FSD \_ \[ 1-5 \]** al calcular la mejor ruta a una red de destino. Por lo tanto, el protocolo de enrutamiento debe asegurarse de que el miembro de **\_ métrica FSD** tenga un valor de métrica adecuado.

Un protocolo de enrutamiento podría usar **las \_ marcas FSD** para marcar una ruta como no válida, si no se debe usar en otros protocolos de enrutamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                        |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de la versión 1 del administrador de tablas de enrutamiento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Estructuras de la versión 1 del administrador de tablas de enrutamiento](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_ruta IP de RTM \_**](rtm-ip-route.md)
</dt> </dl>

 

 





