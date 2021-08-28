---
description: 'Más información sobre: Constantes de identificador no válidas'
title: Constantes de identificador no válidas
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 28a52b2fc7a51572cc7bb78ad7631df41438310a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473281"
---
# <a name="invalid-handle-constants"></a>Constantes de identificador no válidas


_**Se aplica a:** Windows | Windows Servidor_

## <a name="invalid-handle-constants"></a>Constantes de identificador no válidas

Las siguientes constantes indican identificadores no válidos para distintos aspectos de ESE.


| <p>Constante o valor</p> | <p>Descripción</p> | 
|-----------------------|--------------------|
| <p>JET_instanceNil<br />(~(JET_INSTANCE)0)</p> | <p>Identificador no válido para una instancia de base de datos.<br /><strong>Windows XP:</strong> Introducido en Windows XP.</p> | 
| <p>JET_sesidNil<br />(~(JET_SESID)0)</p> | <p>Identificador no válido para un identificador de sesión.</p> | 
| <p>JET_tableidNil<br />(~(JET_TABLEID)0)</p> | <p>Identificador no válido para un identificador de tabla.</p> | 
| <p>JET_bitNil<br />((JET_GRBIT)0)</p> | <p>Identificador no válido para un grupo de bits.</p> | 
| <p>JET_LSNil<br />(~(JET_LS)0)</p> | <p>Identificador no válido para el controlador local Storage.</p> | 
| <p>JET_dbidNil<br />((JET_DBID) 0xFFFFFFFF)</p> | <p>Identificador no válido para el identificador de base de datos.</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 


