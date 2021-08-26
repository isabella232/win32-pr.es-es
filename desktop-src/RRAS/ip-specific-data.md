---
title: IP_SPECIFIC_DATA estructura (Rtm.h)
description: La estructura \_ IP SPECIFIC DATA contiene datos específicos de IP.
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- IP_SPECIFIC_DATA ras de estructura
- PIP_SPECIFIC_DATA de estructura ras
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
ms.openlocfilehash: 906ae9f2accb3d380227f08ad6b65642b96ce6bfa928591bd11a69c478f531b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036675"
---
# <a name="ip_specific_data-structure"></a>Estructura \_ DE DATOS \_ ESPECÍFICOS DE IP

\[Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **estructura IP SPECIFIC \_ DATA** contiene datos específicos de IP.

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

**Tipo \_ FSD**
</dt> <dd>

Especifica el tipo de ruta tal como se define en [RFC 1354.](routing-protocols-request-for-comments.md) En la tabla siguiente se muestran los valores posibles para este miembro.



| Miembro                                                                                               | Significado                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | No se especifica el tipo de ruta. El tipo es diferente de los que se enumeran aquí.<br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | La ruta no es válida. Normalmente, este valor se usa para invalidar una ruta. Sin embargo, dado que el administrador de tablas de enrutamiento no admite la invalidación, la ruta se sigue teniendo en cuenta en los cálculos de mejor ruta. Por lo tanto, los protocolos de enrutamiento no deben usar este valor.<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | La ruta es una ruta local, es decir, el próximo salto es el destino final.<br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | La ruta es una ruta remota, es decir, el próximo salto no es el destino final.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**Directiva de \_ FSD**
</dt> <dd>

Especifica el conjunto de condiciones que provocarían la selección de una ruta de varias rutas de acceso. Este miembro suele estar en formato IP TOS. Para obtener más información, [vea RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**NextHopAS de FSD \_**
</dt> <dd>

Especifica el número de sistema autónomo del próximo salto.

</dd> <dt>

**Prioridad de FSD \_**
</dt> <dd>

Especifica un valor de métrica. El administrador de tablas de enrutamiento usa este valor para comparar esta entrada de ruta con las entradas de ruta obtenidas de otros protocolos de enrutamiento. El valor de este miembro lo establece el administrador de tablas de enrutamiento.

</dd> <dt>

**Métrica de \_ FSD**
</dt> <dd>

Especifica un valor de métrica. El administrador de tablas de enrutamiento usa este valor para comparar esta entrada de ruta con otras entradas de ruta obtenidas del mismo protocolo de enrutamiento. El valor de este miembro lo establece el protocolo de enrutamiento.

</dd> <dt>

**Métrica \_ FSD1**
</dt> <dd>

Especifica un valor de métrica específico del protocolo de enrutamiento. Este valor de métrica se documenta en [RFC 1354.](routing-protocols-request-for-comments.md)

</dd> <dt>

**Métrica \_ FSD2**
</dt> <dd>

Especifica un valor de métrica específico del protocolo de enrutamiento. Este valor de métrica se documenta en [RFC 1354.](routing-protocols-request-for-comments.md)

</dd> <dt>

**Métrica \_ FSD3**
</dt> <dd>

Especifica un valor de métrica específico del protocolo de enrutamiento. Este valor de métrica se documenta en [RFC 1354.](routing-protocols-request-for-comments.md)

</dd> <dt>

**Métrica \_ FSD4**
</dt> <dd>

Especifica un valor de métrica específico del protocolo de enrutamiento. Este valor de métrica se documenta en [RFC 1354.](routing-protocols-request-for-comments.md)

</dd> <dt>

**Métrica \_ FSD5**
</dt> <dd>

Especifica un valor de métrica específico del protocolo de enrutamiento. Este valor de métrica se documenta en [RFC 1354.](routing-protocols-request-for-comments.md)

</dd> <dt>

**Marcas \_ FSD**
</dt> <dd>

Especifica si la ruta es válida. El protocolo de enrutamiento debe borrar primero estas marcas y, a continuación, establecer la ruta como válida o no válida. El protocolo de enrutamiento debe usar las macros **ClearRouteFlags(),** **SetRouteValid() y** **ClearRouteValid()** para realizar estas operaciones. Estas macros se definen en Rtm.h.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El administrador de tablas de enrutamiento usa los **miembros prioridad FSD \_** y métrica **FSD \_** para calcular la mejor ruta a una red de destino determinada.

Los **miembros de la métrica FSD \_ \[ 1-5 \]** son para la conformidad de MIB II. Los agentes de MIB II solo muestran estos valores de métrica. No muestran el valor de métrica **de métrica de FSD. \_** Para que se muestre la métrica **FSD, \_** el protocolo de enrutamiento también debe almacenar el valor en uno de los miembros de la métrica **\_ FSD \[ 1-5. \]**

El administrador de tablas de enrutamiento no usa los valores de métrica en los miembros de la métrica **\_ \[ 1-5 \] de FSD** al calcular la mejor ruta a una red de destino. Por lo tanto, el protocolo de enrutamiento debe asegurarse de que el **miembro métrica \_ FSD** tiene un valor de métrica adecuado.

Un protocolo de enrutamiento podría usar las marcas FSD para marcar una ruta como no válida, si otros **\_ protocolos** de enrutamiento no deben usar la ruta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                        |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>Rtm.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de la versión 1 de Routing Table Manager](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Estructuras de la versión 1 del Administrador de tablas de enrutamiento](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RTM \_ IP \_ ROUTE**](rtm-ip-route.md)
</dt> </dl>

 

 





