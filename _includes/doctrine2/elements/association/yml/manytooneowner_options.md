~~~yaml
itemRecord:
  type: entity
  fields:
  manyToOne:
    ean:
      targetEntity: ean
      inversedBy: itemRecord
      fetch: LAZY
      orphanRemoval: true
      cascade: ["all", "merge", "persist", "refresh", "remove"]
      joinColumns:
        eanId:
          referencedColumnName: id
          unique: true
          onDelete: CASCADE
          onUpdate: RESTRICT
~~~
